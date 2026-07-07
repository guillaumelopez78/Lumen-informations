---
name: Loader
category: Feedback
status: stable
---

# Loader

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/loader
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/loader

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

---

## Guidelines

**Use Loader when**: Operation with **unknown duration** or **no determinable progress**. Specifically:
- **Button states during action** → saving invoice, sending email, processing payment (show in button)
- **Page section loading** → fetching customer details, loading transaction history, rendering dashboard
- **Full-page load** → initial app load, heavy data fetch (full-page overlay with spinner)
- **File operations** → uploading CSV, exporting PDF (unknown completion time)
- **Async operations** → API calls, background processing, webhook waiting

**Don't use Loader when**:
- ❌ Progress determinable (0-100%) → use Progress bar instead
- ❌ Quick operations (<300ms) → delay Loader by 300ms to avoid flicker
- ❌ Offline scenarios → don't show spinner if no network
- ❌ Indefinite/broken operations → show error message, not endless spinner

**Loader placement by context**:
- **In Button**: `<Button loading={true}>Saving...</Button>` (spinner replaces icon)
  - Used for form submissions, "Save", "Send", "Export" buttons
  - Button text shows "Saving…" or "Sending…" while loading
  - Width stays constant (icon-sized spinner fits in same space)
- **In section**: Small spinner with caption "Loading transactions…"
  - Placed above the section that's loading
  - User can still interact with other page content
- **Full-page overlay**: Large spinner for initial page load
  - Covers entire screen with semi-transparent overlay
  - Used sparingly (only for app initialization)
  - Shows optional helpful text: "Loading your dashboard…"

**Timing**:
- **Delay by 300ms before showing** → avoids flicker for quick operations (<300ms)
- **Standard duration**: 3-5 seconds before showing error fallback
- **After 10 seconds**: Show error message with retry option (don't spin forever)

**Variants by size**:
- `size="sm"` (16px) → inline in button, within input, beside form field
- `size="md"` (24px) → section loading, in empty state placeholder
- `size="lg"` (40px) → full-page loader, hero loading state

**Web vs Mobile**:
- Web: standard spinner, show in button or section
- Mobile: same spinner, button loader may be more prominent (larger touch target)
- Mobile: full-page loader centers on screen

**Text pairing**:
- With button: "Saving…", "Sending…", "Exporting…" (verb + ellipsis)
- With section: "Loading invoices…", "Fetching data…"
- With page: "Loading dashboard…" (optional, minimal text)

**When to pair with other components**:
- Loader + Toast → show spinner during action, toast when complete
- Loader + Progress bar → if progress becomes known, switch to progress
- Loader → Error state → "Failed to load. [Retry]" if loading fails

### Imports

**Web**:
```tsx
import { Loader } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Loader } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Loader } from '@shinetools/lumen-react';

// Sizes
<Loader size="sm" />  // default
<Loader size="md" />
<Loader size="lg" />

// Inline in a button
<Button variant="filled" disabled
  startIcon={<Loader size="sm" />}
  label="Saving…"
/>
```

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Inline button spinner + skeleton for content | Large spinner for a quick operation — unnecessary flicker |
| Delay the Loader by **300ms** before showing it — avoids flashing for fast operations | Show the Loader immediately (0ms) — causes unnecessary flickers for operations under 300ms |
| Use locally (button, section) for actions, and as a full-page overlay for complete page loads — both patterns are valid | Always use a global overlay — inline loaders are preferred for localized actions |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Delay the Loader by 300ms before showing it on mobile — same rule | Show Loader immediately on mobile |

---

**For full API, props, variants, tokens**: See GitHub source above.
