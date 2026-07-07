# Icon - Guidelines

## Icon Guidelines

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
| aria-label + Tooltip — screen readers and sighted users both understand | Icon button with no label — screen reader says nothing |
| Default to `size="sm"` (16px) — it's the most common icon size in Shine's interface | Use 20px or 24px for general interface icons — 16px is the standard; reserve larger sizes for navigation and headers |
| Use only Lucide icons (`lucide-react`) — all icons in Shine come from this single library | Use custom SVGs or icons from other libraries — Lucide is the exclusive icon source in Shine |

### Native (Mobile)


> 🔴 To define — Native Icon guidelines not yet documented (Lucide Native TBD).

---

---

### Imports

**Web**:
```tsx
import { Icon } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Icon } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Icon } from '@shinetools/lumen-react';
import { Star, Plus, AlertTriangle } from 'lucide-react';

// Decorative (alongside text)
<Button label="New invoice" startIcon={<Icon icon={Plus} />} />

// Standalone (meaningful)
<Icon
  icon={AlertTriangle}
  size="lg"
  label="Warning"
/>

// Sizes
<Icon icon={Star} size="xs" /> // 12px
<Icon icon={Star} size="sm" /> // 16px
<Icon icon={Star} size="md" /> // 20px — default
<Icon icon={Star} size="lg" /> // 24px
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| aria-label + Tooltip — screen readers and sighted users both understand | Icon button with no label — screen reader says nothing |
| Default to `size="sm"` (16px) — it's the most common icon size in Shine's interface | Use 20px or 24px for general interface icons — 16px is the standard; reserve larger sizes for navigation and headers |
| Use only Lucide icons (`lucide-react`) — all icons in Shine come from this single library | Use custom SVGs or icons from other libraries — Lucide is the exclusive icon source in Shine |

### Native (Mobile)


> 🔴 To define — Native Icon guidelines not yet documented (Lucide Native TBD).

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Icon } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Icon } from '@shinetools/lumen-native';
```
