# System-Banner - Guidelines

## System-Banner Guidelines

### Use Cases
- Primary use case 1
- Primary use case 2
- Primary use case 3
- Primary use case 4

### Best Practices
- Practice 1
- Practice 2
- Practice 3

### Accessibility Requirements
- Follow WCAG AA standards
- Test with screen readers
- Keyboard navigation support required
- Color must not be the only conveyor of meaning


---

## Do / Don't

| ✅ Do | ❌ Don't |
|---|---|
| One System Banner at a time — product-wide, highest urgency only | Stack multiple System Banners — creates noise |
| Use `type="danger" color="primary"` for outages — maximum visibility | Use `primary` color mode for routine announcements |
| Include an action if users need to do something | Leave an action-less `danger` banner — always offer a path forward |

---

---

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

---

## Do / Don't

| ✅ Do | ❌ Don't |
|---|---|
| One System Banner at a time — product-wide, highest urgency only | Stack multiple System Banners — creates noise |
| Use `type="danger" color="primary"` for outages — maximum visibility | Use `primary` color mode for routine announcements |
| Include an action if users need to do something | Leave an action-less `danger` banner — always offer a path forward |

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { System-Banner } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { System-Banner } from '@shinetools/lumen-native';
```
