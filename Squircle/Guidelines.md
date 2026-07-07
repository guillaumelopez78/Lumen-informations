# Squircle - Guidelines

## Guidelines

Superellipse-shaped container for merchant logos, app icons, and entity backdrops. The distinctive rounded-square silhouette of Shine.

### Imports

**Web**:
```tsx
import { Squircle } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Squircle } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Squircle } from '@shinetools/lumen-react';
import { Folder } from 'lucide-react';

// Icon type
<Squircle
  type="icon"
  icon={<Folder />}
  color="accent"
  variant="subtle"
  size="md"
/>

// Letters (initials)
<Squircle
  type="letters"
  letters="AC"
  color="neutral"
  size="sm"
/>

// Avatar (image)
<Squircle
  type="avatar"
  src="/logos/stripe.png"
  size="md"
/>
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Consistent sm (32px) across all list rows | Mixed sizes (16 / 40 / 24 px) — visual noise |
| Use `type="icon" variant="subtle"` in transaction and list rows — it's the primary pattern in Shine | Use `variant="primary"` in dense lists — the subtle background is less distracting in data-heavy contexts |
| Use Squircle to illustrate list item types (categories, transaction types) and for collaborator avatars — these are the two main contexts in Shine | Use Squircle as a decorative element unrelated to content identity |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Use Squircle to illustrate list item types and collaborator avatars on mobile — same as React | |

---
