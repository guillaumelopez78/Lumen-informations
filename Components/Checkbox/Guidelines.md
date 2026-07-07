# Checkbox - Guidelines

## Checkbox-Specific Guidelines

### Use Cases
- **Multi-select forms**: Checkboxes saved via submit button
- **Filtering**: Multiple selection options in a list
- **Agreements**: Accept terms, privacy policy checkboxes
- **Permissions**: Grant multiple simultaneous permissions

### Label & Wording
- Use statements, not questions: "Send weekly reports" not "Do you want updates?"
- Keep labels short and scannable
- Label the feature, not the action
- All caps should be avoided (increases cognitive load)

### State Variations
- **Checked**: User explicitly selected this option
- **Unchecked**: User has not selected this option
- **Indeterminate**: Mixed state in parent (partial selection)
- **Disabled**: Option not available in current context

### Grouping & Organization
- Wrap in `<fieldset>` with `<legend>` for screen readers
- Group related checkboxes visually
- Order: Most common/important first
- Show hint text for each option if complex

### When NOT to Use
- Single boolean in a form: Use Switch instead
- Instant-effect toggle: Use Switch instead
- Form with auto-save: Use Checkbox + submit separately

### Accessibility
- Label must be clickable (large touch target)
- Group label announced before each option
- Indeterminate state conveyed to screen readers
- Keyboard: Tab/Space to select


---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Multi-select group saved on submit | Single immediate-effect setting → use Toggle |
| Let users select items individually — no "Select all" checkbox in generic lists | Add a master "Select all" checkbox to multi-select lists — use the Table component when bulk selection is needed |
| Use just the confirmation button in destructive modals — the modal text + button label is enough confirmation | Add a "I confirm deletion" checkbox before the delete button — the confirmation button already serves that purpose |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Use comfortArea on mobile for larger touch targets | Remove comfortArea on mobile — touch targets need to be larger |

---

---

### Imports

**Web**:
```tsx
import { Checkbox } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Checkbox } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Checkbox } from '@shinetools/lumen-react';

// Uncontrolled
<Checkbox label="Accept terms and conditions" required />

// Controlled
const [checked, setChecked] = useState(false);

<Checkbox
  label="Send me updates"
  checked={checked}
  onChange={(e) => setChecked(e.target.checked)}
/>

// Select all (indeterminate)
<Checkbox
  label="Select all"
  checked={allSelected}
  indeterminate={someSelected}
  onChange={(e) => toggleAll(e.target.checked)}
/>
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Multi-select group saved on submit | Single immediate-effect setting → use Toggle |
| Let users select items individually — no "Select all" checkbox in generic lists | Add a master "Select all" checkbox to multi-select lists — use the Table component when bulk selection is needed |
| Use just the confirmation button in destructive modals — the modal text + button label is enough confirmation | Add a "I confirm deletion" checkbox before the delete button — the confirmation button already serves that purpose |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Use comfortArea on mobile for larger touch targets | Remove comfortArea on mobile — touch targets need to be larger |

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Checkbox } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Checkbox } from '@shinetools/lumen-native';
```
