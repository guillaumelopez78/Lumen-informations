---
name: Dropdown
category: Forms / Navigation
status: stable
---

# Dropdown

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/dropdown
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/dropdown

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟡 WIP | — | Not yet released, coming soon |
| 📱 Mobile (lumen-native) | 🟡 WIP | — | Not yet released, coming soon |

**Recommendation**: Use [[Select]] or [[Menu]] component instead. Dropdown is vault-only at this time.

---

## Guidelines

Generic dropdown trigger + panel. More flexible than [[Select]] — can contain actions, links, or custom content, not just option lists.

### Imports

**Web**:
```tsx
import { Dropdown } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Dropdown } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
<Dropdown />
```

---

## Do / Don't

### React (Web)

| ✅ Do | ❌ Don't |
|---|---|
| [Good practice] | [Bad practice] |
| [Good practice] | [Bad practice] |

### Native (Mobile)

| ✅ Do | ❌ Don't |
|---|---|
| [Good practice] | [Bad practice] |
| [Good practice] | [Bad practice] |

---

**For full API, props, variants, tokens**: See GitHub source above.
