# TextArea - Specs

## Design Tokens

All design tokens follow the Lumen token system. Use CSS variables for dynamic theming.

### Color Tokens
- `--lumen-color-primary` — Primary brand color (#000000)
- `--lumen-color-accent` — Interactive accent (#0066FF)
- `--lumen-color-danger` — Destructive actions (#FF3B30)
- `--lumen-color-neutral-*` — Gray scale
- `--lumen-color-text-primary` — Main text
- `--lumen-color-text-secondary` — Secondary text
- `--lumen-color-surface-*` — Background colors

### Typography Tokens
- `--lumen-font-family-inter` → Inter
- `--lumen-font-size-body-sm` → 12px
- `--lumen-font-size-body-md` → 14px
- `--lumen-font-size-body-lg` → 16px
- `--lumen-font-weight-regular` → 400
- `--lumen-font-weight-semibold` → 600
- `--lumen-line-height-normal` → 1.5

### Spacing Tokens
- `--lumen-padding-*` (6, 8, 10, 12, 14, 16px)
- `--lumen-margin-*` (same scale)
- `--lumen-gap-*` (for flex/grid gaps)

### Size Tokens
- `--lumen-sizing-20` → 20px (small)
- `--lumen-sizing-24` → 24px (medium)
- `--lumen-sizing-32` → 32px (large)
- `--lumen-sizing-40` → 40px (input height)
- `--lumen-sizing-44` → 44px (min touch target)

### Motion Tokens
- `--lumen-motion-fast` → 150ms ease
- `--lumen-motion-standard` → 200ms ease
- `--lumen-motion-slow` → 300ms ease

---

## Tokens Used in TextArea

| Property | Token | Value |
|----------|-------|-------|
| Primary color | `--lumen-color-primary` | #000000 |
| Accent color | `--lumen-color-accent` | #0066FF |
| Border radius | `--lumen-border-radius-sm` | 4px |
| Spacing unit | `--lumen-spacing-8` | 8px |

---

## Component Props

### Common Props
- `variant` — Visual variant (filled, outlined, text)
- `color` — Color scheme (primary, accent, danger)
- `size` — Size variant (small, medium, large)
- `disabled` — Disable interaction
- `loading` — Show loading state
- `aria-label` — Label for screen readers

### Web-Specific Props
- `className` — Custom CSS class
- `style` — Inline styles
- `onClick` — Click handler
- `onFocus` / `onBlur` — Focus handlers

### Mobile-Specific Props
- `testID` — Test identifier
- `onPress` — Press handler
- `accessible` — Accessibility hint

For complete API and TypeScript types:
- 🌐 **Web (React)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/textarea
- 📱 **Mobile (Native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/textarea

---

## Variants

### Visual Variants
- **Filled** — Solid background, primary emphasis (use for main actions)
- **Outlined** — Border only, secondary emphasis (use for secondary actions)
- **Text** — Text only, minimal emphasis (use for tertiary or icon-only)
- **Tonal** — Light background, medium emphasis (use for supporting actions)

### State Variants
- **Default** — Normal state, clickable/interactable
- **Hover** — Subtle background change on pointer hover
- **Active** — Darker state during interaction
- **Focus** — 2px focus ring around element
- **Disabled** — Grayed out, 50% opacity, not clickable
- **Loading** — Spinner animation, button stays same width

### Size Variants
- **Small** — Compact, for dense layouts
- **Medium** — Default, for most contexts
- **Large** — Prominent, for primary CTAs

---

## Related Components

- **Button** ← Main action trigger
- **Checkbox** ← Multi-select (use instead of Button for selection)
- **Switch** ← Instant-effect toggle (not form-based)
- **Link** ← Navigation (use instead of Button for page links)
- **Dialog** ← Confirmation (use with destructive Buttons)
- **Toast** ← Feedback after action (pair with async Button)

---

## Browser & Device Support

| Browser | Version | Support | Notes |
|---------|---------|---------|-------|
| Chrome | Latest | ✅ | Primary target |
| Firefox | Latest | ✅ | Tested |
| Safari | 14+ | ✅ | iOS + macOS |
| Edge | Latest | ✅ | Chromium-based |

| Platform | Version | Support | Notes |
|----------|---------|---------|-------|
| iOS | 14+ | ✅ | Native or React Native |
| Android | API 21+ | ✅ | Native or React Native |
| Web | All modern | ✅ | ES2020+ |
