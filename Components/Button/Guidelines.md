## Visual Examples

![Button Guidelines](./Images/preview-1.png)

**✅ DO:** Primary action on right, accent only for single most important CTA per screen.
**❌ DON'T:** Two Accent buttons on same screen — visual hierarchy disappears.

---

![Button Examples](./Images/preview-2.png)

**✅ DO:** Outlined + filled, clear contrast between secondary and primary.
**❌ DON'T:** Two filled buttons side by side — no visual hierarchy.

---

![Button Actions](./Images/preview-3.png)

**✅ DO:** Verb + noun — "Create invoice", "Add expense" — names the action precisely.
**❌ DON'T:** "Submit", "OK", "Click here" — generic labels that give no context.

---

![Button Loading](./Images/preview-4.png)

**✅ DO:** Use `loading={true}` for every async action — spinner replaces icon, button stays same width.
**❌ DON'T:** Disabled button + separate spinner — unlinked feedback, inconsistent pattern.

---

![Button Icons](./Images/preview-5.png)

**✅ DO:** `variant="text"` + `aria-label` for icon-only buttons — screen readers need a text label.
**❌ DON'T:** A styled `<div>` with no aria-label — invisible to screen readers.

---

![Button Positioning](./Images/preview-6.png)

**✅ DO:** In drawer footer: secondary on left, primary (filled) on right.
**❌ DON'T:** Primary on left — wrong position carries more visual weight.

---

![Button Mobile](./Images/preview-7.png)

**✅ DO:** In button sheet: secondary on top, primary (filled) at bottom.
**❌ DON'T:** Primary at top of stack — button carries more weight on mobile.

---

![Button Inline](./Images/preview-8.png)

**✅ DO:** Primary CTA inside a button sheet only — only valid placement on mobile.
**❌ DON'T:** Primary filled button inline in page content — reserved for button sheets only.

---

![Button Text Variant](./Images/preview-9.png)

**✅ DO:** Icon-only buttons on mobile with `variant="text"` or `variant="tonal"`.
**❌ DON'T:** `variant="filled"` for icon-only buttons — use text or tonal instead.

---

## Do / Don't Quick Reference

| ✅ Do | ❌ Don't |
|---|---|
| One accent button per screen | Multiple accent buttons |
| Pair outlined + filled for hierarchy | Two filled buttons without hierarchy |
| Use action verbs: "Save", "Delete", "Continue" | Generic: "OK", "Submit", "Click here" |
| Use `loading={true}` for async | Disable + separate spinner |
| `variant="text"` + `aria-label` for icon-only | Unstyled `<div>` without aria-label |
| Primary on right in form footer | Primary on left |
| Primary at bottom on mobile | Primary at top |

---

## Imports

```tsx
import { Button } from '@shinetools/lumen-react';
import { Button } from '@shinetools/lumen-native';
```