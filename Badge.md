---
name: Badge
category: Feedback
status: stable
---

# Badge

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/badge
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/badge

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

---

## Guidelines

**Use Badge when**: Small, **non-interactive** status or count indicator. Specifically:
- **Notification counts** → "5" unread messages, "3" new alerts (count mode)
- **Status indicators** → Paid (green dot), Draft (gray dot), Overdue (red dot)
- **System-generated states** → "Active" badge on subscription, "Trial" badge on account
- **Unread indicators** → dot badge on sidebar item, count badge on notification icon
- **Status on list items** → invoice row showing "PAID" badge, customer showing "PREMIUM" badge
- **Achievement/feature badges** → "Pro" badge, "Verified" badge, "Featured" badge

**Don't use Badge when**:
- ❌ Interactive filtering → use Tag component instead (Tag is clickable)
- ❌ User-defined categories → use Tag instead (Badge is system state)
- ❌ Removable labels → use Tag with `onClear()` instead
- ❌ Selectable options → use Radio, Checkbox, or Tag instead
- ❌ Long text labels → Badge is compact only; use Tag or Label for longer text

**Key distinction**:
- **Badge** = system state, read-only, small, non-interactive (Paid, Draft, Active)
- **Tag** = category/filter, interactive, user-selectable, removable (Invoice, Q4, Priority)

**Badge modes by use case**:
- **Count mode**: Numeric count with background
  - `<Badge count={5} color="accent" />` → "5" indicator
  - Use for notifications, unread counts, item counts
  - Shows exact number (don't hide counts in dots)
- **Status mode (dot)**: Single-color dot, no number
  - `<Badge color="success" />` → green dot
  - Use for payment status (Paid, Pending, Failed)
  - Use for subscription status (Active, Paused, Canceled)
  - Use for approval status (Approved, Pending, Rejected)
- **Mode variants**:
  - `mode="primary"` → solid color (most common)
  - `mode="subtle"` → muted/tinted color (secondary status)

**Color semantics**:
- `color="success"` (green) → Paid, Approved, Active, Complete
- `color="danger"` (red) → Failed, Overdue, Canceled, Rejected
- `color="warning"` (orange) → Pending, At-risk, Caution
- `color="accent"` (blue) → Active feature, Highlighted state
- `color="neutral"` (gray) → Draft, Paused, Inactive, Archived

**Behavior**:
- Non-interactive (no click handler)
- No close/dismiss button
- Position: typically top-right or inline with related item
- Updates automatically when state changes (no user action needed)

**Context by page**:
- **Invoice list**: status badge (Paid, Pending, Overdue) on each row
- **Sidebar**: count badge on "Messages" (shows unread count)
- **Header**: count badge on notification icon (shows alert count)
- **Profile card**: status badges (Premium, Verified) below name
- **Tab/section header**: count badge showing items in section

**Web vs Mobile**:
- Web: inline with text or element it describes
- Mobile: same positioning, badges remain small and scannable
- Count badge might increase slightly for touch readability but stay compact

**Pairing**:
- Badge + Icon → dot badge shows status, icon is the thing (notification icon + "5" count)
- Badge + Row item → status badge right-aligned, shows document state
- Badge + Card → small badge in corner or with title
- Badge + Button → notification badge on "Messages" button

### Imports

**Web**:
```tsx
import { Badge } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Badge } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Badge } from '@shinetools/lumen-react';

// Digit badge
<Badge count={3} color="neutral" />
<Badge count={3} color="accent" />
<Badge count={12} color="danger" />

// Solid fill (default)
<Badge count={5} color="warning" mode="primary" />

// Tinted subtle fill
<Badge count={5} color="warning" mode="subtle" />

// Dot (status indicator)
<Badge color="success" /* no count or icon = dot */ />
<Badge color="danger" />
```

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| One semantic badge per row — status at a glance | 4 badge variants on one row — priority unclear |
| Use `count` mode with a number for unread notifications (messages, alerts) — shows the exact count | Use `dot` mode for unread counts — the dot gives no quantity information |
| Leave status badge colors unforced for now — no global convention defined yet, align per-feature | Invent new color meanings without cross-team alignment — wait for the global convention |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Use count mode for unread notifications on mobile — same as React | Use dot mode for unread counts on mobile |

---

**For full API, props, variants, tokens**: See GitHub source above.
