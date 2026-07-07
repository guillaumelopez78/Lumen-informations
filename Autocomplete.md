---
name: Autocomplete
category: Forms
status: stable
---

# Autocomplete

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/autocomplete
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/autocomplete

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟡 WIP | — | Not yet released, coming soon |
| 📱 Mobile (lumen-native) | 🟡 WIP | — | Not yet released, coming soon |

**Recommendation**: Use [[Select]] component with filtering instead. Autocomplete is vault-only at this time.

---

## Guidelines

Text input with dynamic suggestion list. Unlike [[Select]], the user types freely and suggestions update in real time from an async source.

### Imports

**Web**:
```tsx
import { Autocomplete } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Autocomplete } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
<Autocomplete />
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
