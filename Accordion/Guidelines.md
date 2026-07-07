# Accordion - Guidelines

## Accordion Guidelines

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

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| 2 items — first open, second ready to expand | Accordion inside accordion — depth 2 is confusing |
| Allow multiple panels to be open simultaneously — users can expand as many sections as they need | Force exclusive mode (one open at a time) — Shine lets users open multiple panels freely |
| Use Accordion for FAQ/help content, settings sections, and transaction details — all three are valid contexts in the product | Limit Accordion to a single use case — it's a versatile pattern in Shine |

### Native (Mobile)


> 🔴 To define — Native Accordion guidelines not yet documented.

---

---

### Imports

**Web**:
```tsx
import { Accordion } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Accordion } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Accordion } from '@shinetools/lumen-react';

// Basic usage
<Accordion title="What is Shine?" defaultOpen>
  Shine is a business account for French SMEs and freelancers.
</Accordion>
<Accordion title="How do I export transactions?">
  Go to Transactions → Export → CSV or PDF.
</Accordion>

// With divider
<Accordion title="General" showDivider>...content...</Accordion>
<Accordion title="Notifications" showDivider>...content...</Accordion>
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| 2 items — first open, second ready to expand | Accordion inside accordion — depth 2 is confusing |
| Allow multiple panels to be open simultaneously — users can expand as many sections as they need | Force exclusive mode (one open at a time) — Shine lets users open multiple panels freely |
| Use Accordion for FAQ/help content, settings sections, and transaction details — all three are valid contexts in the product | Limit Accordion to a single use case — it's a versatile pattern in Shine |

### Native (Mobile)


> 🔴 To define — Native Accordion guidelines not yet documented.

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Accordion } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Accordion } from '@shinetools/lumen-native';
```
