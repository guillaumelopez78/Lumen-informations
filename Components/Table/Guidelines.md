# Table - Guidelines

## Table Guidelines

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
| Full amounts + semantic badge column | Truncated amount + icon-only actions (inaccessible) |
| Make all columns sortable by default — sorting is always on in Shine tables | Opt-in to sorting per column — all columns are sortable unless explicitly disabled |
| Use a full empty state (illustration + title + description + CTA) when the table has no results — it's the standard in Shine | Show a plain "No results" row or leave the table empty without context or action |

### Native (Mobile)


> 🔴 To define — Native Table guidelines not yet documented.

---

---

### Imports

**Web**:
```tsx
import { Table } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Table } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
type Column = {
  key: string; label: string;
  sortable?: boolean;
  align?: 'left' | 'center' | 'right';
  render?: (value, row) => ReactNode;
}
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Full amounts + semantic badge column | Truncated amount + icon-only actions (inaccessible) |
| Make all columns sortable by default — sorting is always on in Shine tables | Opt-in to sorting per column — all columns are sortable unless explicitly disabled |
| Use a full empty state (illustration + title + description + CTA) when the table has no results — it's the standard in Shine | Show a plain "No results" row or leave the table empty without context or action |

### Native (Mobile)


> 🔴 To define — Native Table guidelines not yet documented.

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Table } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Table } from '@shinetools/lumen-native';
```
