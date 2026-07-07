## Do / Don't

| ✅ Do | ❌ Don't |
|---|---|
| One accent button per screen maximum | Multiple accent buttons on same screen |
| Outlined + filled = clear hierarchy | Two filled buttons without contrast |
| Verb + noun: "Create invoice", "Add expense" | Generic: "Submit", "OK", "Click here" |
| Use `loading={true}` for async actions | Disabled + separate spinner (inconsistent) |
| `variant="text"` + `aria-label` for icon-only | Styled `<div>` without aria-label |
| Secondary on left, primary on right (form footer) | Primary on left (wrong visual weight) |
| Primary at bottom (mobile bottom sheet) | Primary at top (wrong gravity on mobile) |
| Primary CTA inside button sheet only (mobile) | Primary filled button inline in content |
| Icon-only: `variant="text"` or `variant="tonal"` | Icon-only with `variant="filled"` |
| Action verbs with context (e.g. "Save changes") | Single word labels (e.g. just "Save") |

