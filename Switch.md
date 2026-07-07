---
name: Switch
category: Forms
status: stable
---

# Switch

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/switch
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/switch

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

**Note**: Toggle in vault maps to Switch in repository.

---

## Guidelines

Immediate binary switch. Use when the action takes effect instantly, without a submit button. Use Checkbox for form-based selections.

### Imports

**Web**:
```tsx
import { Switch } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Switch } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Switch } from '@shinetools/lumen-react';

// Basic usage
<Switch
  aria-label="Email notifications"
  checked={notifications}
  onCheckedChange={setNotifications}
/>

// Sizes
<Switch aria-label="Push notifications" size="large" checked={push} onCheckedChange={setPush} />
<Switch aria-label="Dark mode" size="compact" checked={dark} onCheckedChange={setDark} />
```

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Descriptive labels — user knows exactly what each toggle controls | "Enable" and "Toggle" — no context for the user |
| Apply changes immediately on toggle — never require a Save button after flipping a Switch | Put a Switch inside a form with a Submit button — use Checkbox for form-based multi-select |
| Use Switch to activate/deactivate collaborator access or permissions — it's the main pattern in Shine for rights management | Show a confirmation modal before applying a Switch toggle — the action should be instantaneous |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Apply changes immediately on toggle, same as React | Require a Save button after toggling a Switch on mobile |
| Use Switch for permissions and access rights on mobile — same pattern as React | |

---

**For full API, props, variants, tokens**: See GitHub source above.
