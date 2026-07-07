# SideNav - Guidelines

## SideNav Guidelines

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
| Grouped sections — scannable in under 2 seconds | 11 ungrouped items — user must read all to find one |
| Keep the SideNav at full width — labels are always visible in the standard Shine interface (icon-only mode is reserved for the Advisor variant) | Implement a collapse toggle for the default SideNav — `collapsed` mode is only used in the `advisor` variant |
| Add badge counters on specific nav items when there is unread or pending content — that's the pattern in Shine | Show badges on all nav items indiscriminately — only display counts where content genuinely requires attention |

### Native (Mobile)


> 🔴 To define — Native navigation pattern not yet documented.

---

---

### Imports

**Web**:
```tsx
import { SideNav } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { SideNav } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
<SideNav />
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Grouped sections — scannable in under 2 seconds | 11 ungrouped items — user must read all to find one |
| Keep the SideNav at full width — labels are always visible in the standard Shine interface (icon-only mode is reserved for the Advisor variant) | Implement a collapse toggle for the default SideNav — `collapsed` mode is only used in the `advisor` variant |
| Add badge counters on specific nav items when there is unread or pending content — that's the pattern in Shine | Show badges on all nav items indiscriminately — only display counts where content genuinely requires attention |

### Native (Mobile)


> 🔴 To define — Native navigation pattern not yet documented.

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { SideNav } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { SideNav } from '@shinetools/lumen-native';
```
