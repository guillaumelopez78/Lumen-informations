# Button - Guidelines

## Button-Specific Guidelines

### Hierarchy & Context
- **Primary CTA**: One `accent` button per screen maximum
- **Secondary action**: `outlined` button for Cancel/Skip/Go back
- **Tertiary action**: `text` button for Learn more/View docs
- **Destructive action**: `danger` button only in confirmation dialogs

### Label Best Practices
- Use action verbs: "Save changes", "Add expense", "Delete invoice"
- Be specific: "Continue to checkout" not just "Continue"
- Avoid generic labels: "OK", "Submit", "Click here"
- Show verb in loading state: "Saving…", "Sending…"

### Layout Patterns
- **Form footer**: Cancel (left, outlined) + Primary (right, accent)
- **Modal footer**: Cancel (left) + Destructive action (right, danger)
- **Toolbar**: Primary action centered, secondary actions on sides
- **Mobile**: Primary CTA always bottom (thumb-reach gravity)

### Accessibility
- Icon-only buttons require `aria-label`
- Loading state must disable interaction
- Focus visible at all times (keyboard navigation)
- Touch targets minimum 44px height
- Color alone must not convey meaning

### Async Patterns
- Use `loading={true}` with text update ("Saving…")
- Disable button while loading (prevent double-click)
- Show inline error or toast on failure
- Clear success feedback after 2-3 seconds


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

---

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


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Button } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Button } from '@shinetools/lumen-native';
```
