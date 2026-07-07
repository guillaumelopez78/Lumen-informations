# Loader - Guidelines

## Loader Guidelines

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
| Inline button spinner + skeleton for content | Large spinner for a quick operation — unnecessary flicker |
| Delay the Loader by **300ms** before showing it — avoids flashing for fast operations | Show the Loader immediately (0ms) — causes unnecessary flickers for operations under 300ms |
| Use locally (button, section) for actions, and as a full-page overlay for complete page loads — both patterns are valid | Always use a global overlay — inline loaders are preferred for localized actions |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Delay the Loader by 300ms before showing it on mobile — same rule | Show Loader immediately on mobile |

---

---

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


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Loader } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Loader } from '@shinetools/lumen-native';
```
