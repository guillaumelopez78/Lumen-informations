# Alert - Guidelines

## Alert Guidelines

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
| Use `danger` for blocking errors that prevent progression | Use `danger` for mild warnings |
| Include a resolution path (`action`) when applicable | Show an error with no way to fix it |
| Keep body copy concise | Write long paragraphs inside an Alert |

---

---

### Imports

**Web**:
```tsx
import { Alert } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Alert } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
<Alert />
```

---

---

## Do / Don't

| ✅ Do | ❌ Don't |
|---|---|
| Use `danger` for blocking errors that prevent progression | Use `danger` for mild warnings |
| Include a resolution path (`action`) when applicable | Show an error with no way to fix it |
| Keep body copy concise | Write long paragraphs inside an Alert |

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Alert } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Alert } from '@shinetools/lumen-native';
```
