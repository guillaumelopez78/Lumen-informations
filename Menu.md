---
name: Menu
category: Navigation
status: stable
---

# Menu

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/menu
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/menu

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟡 WIP | — | Use Select or Dialog instead |

---

## Guidelines

**Use Menu when**: Contextual action list triggered by click/right-click. Specifically:
- **Row actions in table** → "More actions" button on invoice row: View, Duplicate, Edit, Delete
- **Bulk actions** → "More" menu in selected rows: Export, Archive, Change status
- **Card/item actions** → "…" button on card showing Edit, Share, Move, Delete
- **Toolbar overflow** → additional actions that don't fit in button bar
- **Context menu** → right-click on transaction to Share, Export, Flag, Archive

**Don't use Menu when**:
- ❌ Primary navigation → use SideNav, Tabs, or Breadcrumbs instead
- ❌ Page-level actions → use button bar or action toolbar
- ❌ Single action → just use a Button, don't make a menu for one item
- ❌ Many options (8+) → consider reorganizing; large menus are hard to scan
- ❌ Conditional actions only → if item is disabled, just disable it (don't hide)

**Menu structure by context**:
- **Table row menu** → 3-5 actions, organized by impact
  - Safe actions first: View, Duplicate, Details
  - Destructive actions last: Delete, Archive
  - Divider between safe and risky groups
- **Card menu** → 2-4 quick actions
  - Example: Edit, Duplicate, Delete
- **Toolbar menu** → overflow actions from button bar
  - Example: additional sort options, view modes, advanced filters

**Behavior**:
- Trigger: Click "…" button, icon button, or right-click context menu
- Positioning: below/above trigger based on space available
- Keyboard: Tab to trigger, Enter/Space to open, Arrow keys to navigate, Escape to close
- Dismiss: click item, click outside, or press Escape

**Menu item types**:
- **Action item**: Performs action immediately (click → action fires → menu closes)
  - Example: "Duplicate", "Export", "Send reminder"
- **Destructive item**: Dangerous action (shown in red)
  - Example: "Delete" (often triggers Dialog confirmation)
- **Disabled item**: Grayed out, no hover, can't click
  - Example: "Approve" when already approved
- **Checkbox item**: Toggle state within menu (rare)
  - Example: "Mark as read" (toggles read state)

**Labels**:
- Use verbs: "Delete", "Export", "Send", not "Deletion", "Exported"
- Be specific: "Delete invoice" not just "Delete" (if not obvious)
- Destructive in red: visually distinct "Delete", "Archive", "Revoke"

**Web vs Mobile**:
- Web: click "…" button, menu appears near cursor
- Mobile: menu appears as bottom sheet or dropdown (platform-dependent)
- Mobile: full-width options for easier tapping

**Pairing**:
- Menu item (destructive) + Modal → "Delete" → Dialog confirmation → destructive action
- Menu item + Toast → action fires → toast confirms "Invoice deleted"
- Menu item + Drawer → "Edit" → opens side panel editor

**Organizing menu items**:
1. Safe, common actions first (View, Duplicate)
2. Divider
3. State-changing actions (Status, Priority, Tags)
4. Divider
5. Destructive actions (Delete, Archive)

### Imports

**Web**:
```tsx
import { Menu } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Menu } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
<Menu />
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
