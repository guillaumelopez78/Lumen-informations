---
name: Icon
category: Assets
status: stable
---

# Icon

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/icon
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/icon

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

---

## Guidelines

Icon component powered by Lucide — 1 500+ open-source SVG icons. Available in 5 sizes. Always use currentColor so icons inherit their context color.

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

**For full API, props, variants, tokens**: See GitHub source above.
