# Progress - Guidelines

## Guidelines

Displays progress toward a goal. Three types: `determinate` (known %, fills smoothly), `indeterminate` (unknown duration, animates continuously), `segmented` (discrete steps). Use [[Loader]] for spinners.

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
