# Badge - Guidelines

## Badge Guidelines

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
| One semantic badge per row — status at a glance | 4 badge variants on one row — priority unclear |
| Use `count` mode with a number for unread notifications (messages, alerts) — shows the exact count | Use `dot` mode for unread counts — the dot gives no quantity information |
| Leave status badge colors unforced for now — no global convention defined yet, align per-feature | Invent new color meanings without cross-team alignment — wait for the global convention |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Use count mode for unread notifications on mobile — same as React | Use dot mode for unread counts on mobile |

---

---

### Imports

**Web**:
```tsx
import { Badge } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Badge } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Badge } from '@shinetools/lumen-react';

// Digit badge
<Badge count={3} color="neutral" />
<Badge count={3} color="accent" />
<Badge count={12} color="danger" />

// Solid fill (default)
<Badge count={5} color="warning" mode="primary" />

// Tinted subtle fill
<Badge count={5} color="warning" mode="subtle" />

// Dot (status indicator)
<Badge color="success" /* no count or icon = dot */ />
<Badge color="danger" />
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| One semantic badge per row — status at a glance | 4 badge variants on one row — priority unclear |
| Use `count` mode with a number for unread notifications (messages, alerts) — shows the exact count | Use `dot` mode for unread counts — the dot gives no quantity information |
| Leave status badge colors unforced for now — no global convention defined yet, align per-feature | Invent new color meanings without cross-team alignment — wait for the global convention |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Use count mode for unread notifications on mobile — same as React | Use dot mode for unread counts on mobile |

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Badge } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Badge } from '@shinetools/lumen-native';
```
