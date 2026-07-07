---
name: Toast
category: Feedback
status: stable
---

# Toast

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/toast
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/toast

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

---

## Guidelines

**Use Toast when**: Non-blocking action feedback that auto-dismisses. Specifically:
- **Success confirmations** → "Invoice sent", "Changes saved", "Duplicate created"
- **Action results** → "File exported as PDF", "Team member added"
- **Non-critical errors** → "Connection lost, retrying…" (user can continue working)
- **Optional feedback** → showing optional next steps ("View invoice" link after send)

**Don't use Toast when**:
- ❌ Blocking errors → use Banner or Modal instead (modal for critical, banner for page-level)
- ❌ Persistent warnings → use Banner (stays visible until dismissed)
- ❌ User input required → use Dialog or Alert (toast is fire-and-forget)
- ❌ Multiple toasts at once → max 1 toast per action (stack by time, don't pile up)

**Toast variants by use case**:
- `toast.success()` → action completed successfully
- `toast.warning()` → proceed with caution, but action worked
- `toast.danger()` → action failed, but not blocking (e.g., "Retry available")
- `toast.info()` → FYI message (rarely used in business apps)

**Behavior**:
- Auto-dismiss after **5 seconds** (standard duration in Shine)
- Optional action button: `{ label: 'Undo', onClick: () => ... }`
- Position: **bottom-right** on web, **bottom center** on mobile
- Tone: past-tense, factual. "Invoice sent" not "Your invoice has been successfully sent!" (no congratulations)

**Web vs Mobile**: Same 5-second duration. Position changes: web (bottom-right), mobile (bottom-center).

**When to pair with other components**:
- Toast after form submit (success feedback)
- Toast + Banner (if error is critical, show banner; if just feedback, use toast)
- Never Modal + Toast (modal is blocking, toast is not)

### Imports

**Web**:
```tsx
import { Toast } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Toast } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { toast } from '@shinetools/lumen-react';

toast.success('Invoice sent', {
  action: { label: 'View', onClick: () => navigate('/invoices/123') }
});
toast.danger('Export failed — try again');
```

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Action confirmation + optional "View" link | Persistent error → auto-dismiss before user can act |
| States what happened. Object + past-tense verb. Full stop. | Congratulatory tone is patronising for business software. Exclamation marks add noise. |
| Auto-dismiss after **5 seconds** — standard duration in Shine | Use durations under 3s or over 10s — 5s is the confirmed default |
| Display Toasts in the **bottom-right** corner of the screen | Place Toasts at the top or centered — bottom-right is the established position in Shine |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Auto-dismiss after 5 seconds on mobile — same duration as React | |
| Display Toast at the bottom of the screen on mobile | Place Toast at the top — bottom is the confirmed position |

---

**For full API, props, variants, tokens**: See GitHub source above.
