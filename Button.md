---
name: Button
category: Actions
status: stable
---

# Button

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/button
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/button

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

---

## Guidelines

**Use Button when**: Triggering actions or navigation. The fundamental interactive element in Lumen. Always pill-shaped with specific variants by context.

**Button hierarchy by context**:
- **Primary CTA (1 per screen max)**: `filled + accent` (blue)
  - The ONE main action user should take: "Save changes", "Send invoice", "Create company"
  - In form footers: position on right (reading order) or bottom (mobile)
  - In modals: destructive modals use `filled + danger` (red) instead
- **Default action**: `filled + primary` (black)
  - Secondary actions on screen: "Add line item", "Upload file", "Select template"
  - Multiple filled buttons allowed if hierarchy is clear (one is primary)
- **Secondary action**: `outlined + primary` (black outline)
  - De-emphasize but show clearly: "Cancel", "Skip", "Maybe later"
  - In form footers: position on left (paired with primary)
- **Tertiary action**: `text + primary` (underlined text)
  - Low priority: "Learn more", "View docs", "See example"
  - Icon-only buttons (without label): must use `text` variant with `aria-label`
- **Destructive action**: `filled + danger` (red)
  - Permanent/risky actions: "Delete invoice", "Revoke access", "Close account"
  - Usually in Dialog confirmation (hard stop for user)
  - Always requires explicit confirmation (not just a click)

**Context by page/pattern**:
- **Form footer** (signup, checkout, settings)
  - Left: `outlined` "Cancel" or "Skip"
  - Right: `filled + accent` "Save" or "Continue"
  - Both full-width on mobile, auto-width on web
- **Modal footer** (destructive confirmation)
  - Left: `outlined` "Cancel"
  - Right: `filled + danger` "Delete" (or appropriate verb)
- **Table row actions**
  - Edit: `text` or small `filled`
  - Delete: small `filled + danger` or menu item
- **Toolbar/header**
  - Primary action (centered/prominent): `filled + accent`
  - Secondary actions: `outlined` or `text`
- **Bottom sheet (mobile)**
  - Primary CTA at bottom (full-width, `filled + accent`)
  - Secondary at top or left

**Label guidelines**:
- Use infinitive verbs: "Save changes", "Add contact", "Delete file"
- Contextual when possible: "Save changes" not just "Save"
- Past-tense for loading: "Saving…", "Sending…" (not "Save…")
- No generic labels: avoid "OK", "Submit", "Click here"
- Specific outcomes: "Continue to checkout" not just "Continue"

**Variants**:
- `variant="filled"` → solid color, primary emphasis
- `variant="outlined"` → border only, secondary emphasis
- `variant="text"` → text only, lowest emphasis (good for "Learn more", icon-only)
- `loading={true}` → spinner animation, disables button, text changes to "…ing"
- `disabled={true}` → grayed out, no interaction (use for unavailable actions)

**Web vs Mobile**:
- Web: buttons auto-width, grouped horizontally in footers/toolbars
- Mobile: buttons full-width in sticky footer (bottom sheet pattern)
- Mobile: primary CTA always bottom-most (gravity/thumb reach)
- Touch targets minimum 44px height (maintain on mobile)

**Async operations**:
- Use `loading={true}` for submit buttons during async actions
- Spinner replaces icon, button width stays constant
- Disable button while loading (prevent double-clicks)
- Show "Saving…" or "Sending…" text during load

**When NOT to use Button**:
- ❌ Text link to another page → use Link component
- ❌ Toggle setting (on/off) → use Toggle component
- ❌ Multiple exclusive choices → use RadioButton or Checkbox
- ❌ Opening menu → use Menu component (though it has trigger button)

### Imports

**Web**:
```tsx
import { Button } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Button } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
// Primary CTA (one per screen max)
<Button variant="filled" color="accent">
  Save Changes
</Button>

// Default action
<Button variant="filled" color="primary">
  Click me
</Button>

// Secondary action
<Button variant="outlined" color="primary">
  Cancel
</Button>

// Low emphasis
<Button variant="text" color="primary">
  Learn more
</Button>

// Destructive action
<Button variant="filled" color="danger">
  Delete
</Button>

// Async action
<Button variant="filled" loading={isLoading}>
  Saving...
</Button>
```

---

## Do / Don't

### React (Web)

| ✅ Do | ❌ Don't |
|---|---|
| Use `filled + accent` for ONE primary CTA per screen | Place multiple blue (`accent`) buttons on same screen |
| Pair `outlined` + `filled` — clear hierarchy contrast | Place two `filled` buttons side by side without hierarchy |
| In **drawer/modal footers**: secondary on left, primary on right, both full-width | Place primary button on left in drawer/modal |
| In **bottom sheet footers**: secondary on top, primary at bottom, stacked | Place primary button at top of bottom sheet footer |
| Use `loading={true}` for async operations — spinner replaces icon, width stays same | Disable button + show separate spinner somewhere else |
| Use `variant="text"` + `aria-label` for icon-only buttons | Use unstyled `<div>` as button — inaccessible |
| Use infinitive verbs: "Add item", "Save changes" | Use generic labels: "Submit", "OK", "Click here" |
| Include context in labels when space allows | Make labels too short to understand the action |

### Native (Mobile)

| ✅ Do | ❌ Don't |
|---|---|
| Place primary CTA buttons **inside bottom sheet footer** — this is the primary action zone on mobile | Place primary filled buttons inline in page content |
| Use `variant="text"` or `variant="tonal"` for icon-only actions | Use `variant="filled"` for icon-only buttons |
| Use clear labels even on mobile — context matters | Abbreviate labels to save space on mobile screens |

---

**For full API, props, variants, tokens**: See GitHub source above.
