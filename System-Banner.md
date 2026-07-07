---
name: System-Banner
category: Feedback
status: stable
---

# System-Banner

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/system-banner
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/system-banner

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟡 WIP | — | Mobile pattern differs |

---

## Guidelines

Full-width top-of-page system-level alert. Distinct from [[Banner]] (which is page-context) — System Banner is reserved for product-wide announcements, outage notices, and global alerts. Supports `subtle` (tinted) and `primary` (bold, high-contrast) color modes.

### Imports

**Web**:
```tsx
import { System Banner } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { System Banner } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { SystemBanner } from '@shinetools/lumen-react';

// Info announcement (default)
<SystemBanner message="New feature: bulk invoice export is now available." />

// Outage notice
<SystemBanner
  type="danger"
  color="primary"
  message="Payment processing is temporarily unavailable."
  primaryAction={{ label: 'Check status', onClick: () => window.open('https://status.shine.fr') }}
/>

// Maintenance with dismiss
<SystemBanner
  type="warning"
  message="Scheduled maintenance on Sunday 2–4 AM. Some features will be unavailable."
  onDismiss={() => dismiss()}
/>
```

---

## Do / Don't

| ✅ Do | ❌ Don't |
|---|---|
| One System Banner at a time — product-wide, highest urgency only | Stack multiple System Banners — creates noise |
| Use `type="danger" color="primary"` for outages — maximum visibility | Use `primary` color mode for routine announcements |
| Include an action if users need to do something | Leave an action-less `danger` banner — always offer a path forward |

---

**For full API, props, variants, tokens**: See GitHub source above.
