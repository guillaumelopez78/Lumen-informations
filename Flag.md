---
name: Flag
category: Assets
status: stable
---

# Flag

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/flag
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/flag

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

---

## Guidelines

Country flag image wrapper. Displays a national flag by ISO 3166-1 alpha-2 country code. Added in lumen-react v0.13.0.

### Imports

**Web**:
```tsx
import { Flag } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Flag } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Flag } from '@shinetools/lumen-react';

<Flag code="FR" />
<Flag code="DE" size="small" />
<Flag code="US" size="large" alt="United States" />

// Decorative (country name already visible)
<Flag code="GB" alt="" />
```

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Pair with visible country name text for full context | Use flag alone without a country name label — accessibility risk |
| Use `alt="France"` (full name) rather than `alt="FR"` when writing explicit alt text | Use the raw ISO code as `alt` when the full name is available |

---

**For full API, props, variants, tokens**: See GitHub source above.
