---
name: Dialog
category: Overlay
status: stable
---

# Dialog

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/dialog
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/dialog

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

**Note**: Modal in vault maps to Dialog in repository.

---

## Guidelines

**Use Dialog when**: Critical confirmations that BLOCK user flow. Specifically:
- **Destructive confirmations** → delete invoice, revoke API key, close account (must be explicit)
- **Blocking errors** → payment failed, insufficient balance, invalid VAT (user can't proceed without action)
- **Rare critical dialogs** → account suspension warning (very limited use)
- **Permission blocking** → 2FA verification before sensitive action (only when required)

**Don't use Dialog when**:
- ❌ Multi-step form → use Drawer (side panel) instead
- ❌ Simple messages (not blocking) → use Toast (auto-dismiss) or Banner (persistent)
- ❌ Non-critical feedback → use Alert (inline) on the page
- ❌ Lightweight actions → use inline confirm or Popover
- ❌ Selection from list → use Drawer or Dropdown Menu instead

**Key pattern**: Dialog = blocking flow. Drawer = non-blocking side task. Toast = fire-and-forget feedback.

**Web specifics**:
- Standard width: **600px (md)** — all destructive confirmations use this size
- Position: centered on screen, overlay darkens background
- Overlay click closes dialog (always enabled in Shine)
- Footer: secondary button (text/outlined) on left, primary (filled/danger) on right

**Mobile specifics**:
- Use fullscreen Dialog for complex confirmations on mobile
- Overlay click always closes (same as web)
- Buttons: secondary on top, primary at bottom, full-width stacked

### Imports

**Web**:
```tsx
import { Dialog } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Dialog (Modal) } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Modal } from '@shinetools/lumen-react';

<Modal open={open} onClose={() => setOpen(false)}
  title="Delete invoice" size="sm"
  footer={<>
    <Button variant="text" onClick={() => setOpen(false)}>Cancel</Button>
    <Button variant="filled" color="danger" onClick={del}>Delete</Button>
  </>}
>This action cannot be undone.</Modal>
```

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| 1 cancel + 1 danger CTA — clear destructive action | 3 equal-weight accent buttons — user can't prioritize |
| Affirmative title naming the object · consequence in body · Return not Cancel | Question title · vague body · "Yes, delete" adds nothing |
| Modal footer: secondary (`text`/`outlined`) on the left, primary `filled` on the right (inline, auto-width) | Place the primary button on the left — visual weight and reading order both point right |
| Allow closing by clicking the overlay — it's always enabled in Shine | Block overlay close for destructive modals — the overlay always closes the modal in Shine |
| Default to **600px** width (`md`) — the standard modal size in Shine | Use custom widths without a design reason — 600px is the confirmed default |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Overlay click always closes the Modal on mobile — same as React | Block overlay close on mobile |
| Use fullscreen Modal on mobile for complex flows | Use a 600px-wide modal on mobile — use fullscreen instead |

---

**For full API, props, variants, tokens**: See GitHub source above.
