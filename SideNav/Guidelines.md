# SideNav - Guidelines

## Guidelines

Primary application navigation — persistent left panel with main menu, account info, and contextual sections. The root navigation frame for all Shine surfaces.

### Imports

**Web**:
```tsx
import { SideNav } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { SideNav } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
<SideNav />
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Grouped sections — scannable in under 2 seconds | 11 ungrouped items — user must read all to find one |
| Keep the SideNav at full width — labels are always visible in the standard Shine interface (icon-only mode is reserved for the Advisor variant) | Implement a collapse toggle for the default SideNav — `collapsed` mode is only used in the `advisor` variant |
| Add badge counters on specific nav items when there is unread or pending content — that's the pattern in Shine | Show badges on all nav items indiscriminately — only display counts where content genuinely requires attention |

### Native (Mobile)


> 🔴 To define — Native navigation pattern not yet documented.

---
