# Progress - Guidelines

## Progress Guidelines

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
| Use `determinate` when you know the percentage — gives concrete feedback | Use `indeterminate` when you have the percentage — wastes information |
| Use `segmented` for onboarding steps (`value={2}`, `segments={4}` = step 2 of 4) | Use `segmented` for file uploads — misleads about granularity |
| Provide `label="Uploading files"` for screen readers | Leave `label` empty on an indeterminate bar |

---

---

### Imports

**Web**:
```tsx
import { Progress } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Progress } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Progress } from '@shinetools/lumen-react';

// Determinate (file upload at 67%)
<Progress value={67} label="Uploading files" />

// Indeterminate (background sync)
<Progress type="indeterminate" label="Syncing transactions" />

// Segmented (onboarding step 2 of 4)
<Progress type="segmented" value={2} segments={4} label="Step 2 of 4" />

// Accent colour
<Progress value={45} variant="accent" size="medium" />

// On dark background
<Progress value={80} variant="invert" />
```

---

---

## Do / Don't

| ✅ Do | ❌ Don't |
|---|---|
| Use `determinate` when you know the percentage — gives concrete feedback | Use `indeterminate` when you have the percentage — wastes information |
| Use `segmented` for onboarding steps (`value={2}`, `segments={4}` = step 2 of 4) | Use `segmented` for file uploads — misleads about granularity |
| Provide `label="Uploading files"` for screen readers | Leave `label` empty on an indeterminate bar |

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Progress } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Progress } from '@shinetools/lumen-native';
```
