# Flag - Guidelines

## Flag Guidelines

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
| Pair with visible country name text for full context | Use flag alone without a country name label — accessibility risk |
| Use `alt="France"` (full name) rather than `alt="FR"` when writing explicit alt text | Use the raw ISO code as `alt` when the full name is available |

---

---

### Imports

**Web**:
```tsx
import { Flag } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Flag } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Flag } from '@shinetools/lumen-react';

<Flag code="FR" />
<Flag code="DE" size="small" />
<Flag code="US" size="large" alt="United States" />

// Decorative (country name already visible)
<Flag code="GB" alt="" />
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Pair with visible country name text for full context | Use flag alone without a country name label — accessibility risk |
| Use `alt="France"` (full name) rather than `alt="FR"` when writing explicit alt text | Use the raw ISO code as `alt` when the full name is available |

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Flag } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Flag } from '@shinetools/lumen-native';
```
