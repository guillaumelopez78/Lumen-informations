---
name: Divider
category: Layout
status: stable
---

# Divider

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/divider
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/divider

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

---

## Guidelines

Visual separator between content sections or list items.

### Imports

**Web**:
```tsx
import { Divider } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Divider } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Divider } from '@shinetools/lumen-react';

<Divider />                                   // sm, medium
<Divider size="xs" visibility="low" />        // hairline, faint
<Divider size="lg" visibility="high" />       // thick, prominent
```

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Divider between distinct sections — clear grouping | Divider between every list item — use padding instead |
| Default to `size="sm"` and `visibility="low"` — these are the most used combinations in Shine | Use `high` visibility or large sizes by default — keep Dividers discreet |
| Use Dividers both between page sections and inside components (Cards, Menus, Sidebars) — both are valid contexts | Avoid Dividers inside components — they are appropriate in both page-level and component-level layouts |

### Native (Mobile)


> 🔴 To define — Native Divider guidelines not yet documented.

---

**For full API, props, variants, tokens**: See GitHub source above.
