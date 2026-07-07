---
name: Avatar
category: Data display
status: stable
---

# Avatar

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/avatar
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/avatar

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟡 WIP | — | Not yet released, coming soon |
| 📱 Mobile (lumen-native) | 🟡 WIP | — | Not yet released, coming soon |

**Recommendation**: Coming in next release. Design is complete, implementation pending.

---

## Guidelines

Represents a user, organisation, or entity. Used in tables, comments, nav headers, and activity feeds.

### Imports

**Web**:
```tsx
import { Avatar } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Avatar } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
<AvatarGroup max={4}>
  <Avatar name="Alice Martin" src="..." />
  <Avatar name="Bob Chen" src="..." />
  <Avatar name="Carla Diaz" />
</AvatarGroup>
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
