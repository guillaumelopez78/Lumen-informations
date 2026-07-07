# Divider - Guidelines

## Divider Guidelines

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
| Divider between distinct sections — clear grouping | Divider between every list item — use padding instead |
| Default to `size="sm"` and `visibility="low"` — these are the most used combinations in Shine | Use `high` visibility or large sizes by default — keep Dividers discreet |
| Use Dividers both between page sections and inside components (Cards, Menus, Sidebars) — both are valid contexts | Avoid Dividers inside components — they are appropriate in both page-level and component-level layouts |

### Native (Mobile)


> 🔴 To define — Native Divider guidelines not yet documented.

---

---

### Imports

**Web**:
```tsx
import { Divider } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Divider } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Divider } from '@shinetools/lumen-react';

<Divider />                                   // sm, medium
<Divider size="xs" visibility="low" />        // hairline, faint
<Divider size="lg" visibility="high" />       // thick, prominent
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Divider between distinct sections — clear grouping | Divider between every list item — use padding instead |
| Default to `size="sm"` and `visibility="low"` — these are the most used combinations in Shine | Use `high` visibility or large sizes by default — keep Dividers discreet |
| Use Dividers both between page sections and inside components (Cards, Menus, Sidebars) — both are valid contexts | Avoid Dividers inside components — they are appropriate in both page-level and component-level layouts |

### Native (Mobile)


> 🔴 To define — Native Divider guidelines not yet documented.

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Divider } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Divider } from '@shinetools/lumen-native';
```
