---
name: Banner
category: Feedback
status: stable
---

# Banner

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/banner
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/banner

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

---

## Guidelines

**Use Banner when**: Full-width persistent messages at the **very top of the page**. Specifically:
- **System-level warnings** → "Maintenance window 2pm-3pm CET tomorrow" (affects all users/page)
- **Critical page-blocking errors** → "Database backup in progress, read-only mode until 14:00" (affects entire page)
- **Account status alerts** → "Trial expires in 2 days — upgrade now", "Payment failed, service suspended"
- **Persistent status** → "You are in demo mode" (stays visible until dismissed or resolved)
- **Action required (critical)** → "Security verification needed before checkout" (must be acknowledged)

**Don't use Banner when**:
- ❌ Temporary feedback → use Toast (auto-dismiss)
- ❌ Inline field/form error → use Alert (inline where error occurs)
- ❌ Critical blocking action → use Dialog (hard stop)
- ❌ Non-critical info → use Alert (stays in layout flow)
- ❌ Section-level message → use Alert instead (not full-width)

**Banner variants by severity**:
- `error`: System failure or critical block. Page is affected.
  - "Database unreachable — service temporarily offline"
  - "Payment processing failed — service degraded, retry in 5 min"
- `warning`: Action required but page is functional. User should act soon.
  - "Trial expires in 2 days — upgrade to continue"
  - "2FA disabled — re-enable for security"
  - "Invoice overdue by 30 days — send reminder?"
- `success`: Action system-wide success. Rare in business apps.
  - Avoid for post-action feedback (use Toast instead)
  - Only for system events: "Migration completed successfully"

**Behavior**:
- **Always at the very top of viewport** — above all content
- Full-width, sticky (stays visible when scrolling)
- Includes action button when user can immediately resolve
  - Example: "Trial expires soon [Upgrade] [Dismiss]"
- Optional dismiss button (always present for non-critical)
- One banner per page (multiple banners confuse priority)

**Position on page**:
- ALWAYS above the page header/navbar
- Above the page title
- Above sidebars and main content
- Pushes all other content down (not overlay)

**Web vs Mobile**:
- Web: full viewport width, sticky at top
- Mobile: full viewport width, sticky at top (same as web)
- Text wraps on mobile (message is concise and readable)

**Pairing with other feedback**:
- Banner (system state) + Toast (action feedback) = comprehensive feedback
- Banner (critical error) + Alert (field error) = system + field-level clarity
- Never Modal + Banner (modal interrupts the whole page)

**Text tone**:
- Factual, not apologetic: "Service is down" not "We're sorry the service is down"
- Action-oriented: "Upgrade to continue" not "You should probably upgrade"
- Time-specific when applicable: "Trial expires in 2 days" not "Trial expiring soon"

### Imports

**Web**:
```tsx
import { Banner } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Banner } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Banner } from '@shinetools/lumen-react';

// Variants
<Banner variant="success" message="Invoice sent successfully." />
<Banner variant="warning" message="Account balance below €100." />
<Banner variant="error" message="Payment failed — update your method." />

// With title and action
<Banner
  variant="warning"
  title="Balance low"
  message="Balance below €100."
  actionLabel="Top up"
  onAction={topUp}
/>
```

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| One banner, top of page — clear priority | 3 stacked banners — user can't tell what matters most |
| Place Banners above the page header, at the very top of the viewport — above everything else | Place a Banner below the header or inside a section — it belongs at the very top of the page |
| Use `warning` and `error` variants — these are the primary use cases for Banner in Shine | Use `success` for action confirmations — prefer a Toast for post-action success feedback |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Place Banner above the app header on mobile — sticky at the very top | Place Banner inside scroll content on mobile |

---

**For full API, props, variants, tokens**: See GitHub source above.
