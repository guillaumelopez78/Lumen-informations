---
name: Checkbox
category: Forms
status: stable
---

# Checkbox

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/checkbox
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/checkbox

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

---

## Guidelines

**Use Checkbox when**: Multi-select choices OR independent boolean options that are **submitted together**. Specifically:
- **Multi-select in forms** → "Select invoices to export" (checkboxes in a form, submit button at end)
- **Feature toggles (deferred)** → "Email notifications" checkbox in settings (saved on form submit, not immediate)
- **Agreement/consent** → "I accept terms and conditions" (binary choice with form submission)
- **Optional fields** → "Include payment notes in receipt?" (saved with form)
- **Filtered item selection** → select specific invoice items to duplicate/export

**Don't use Checkbox when**:
- ❌ Immediate effect (no submit) → use Toggle instead (immediate state change)
- ❌ Single mutually-exclusive choice → use RadioButton or Select
- ❌ Many options (5+) → consider if checkboxes are right; consider collapsing with "Select all"
- ❌ In large tables without deliberate selection UX → prefer table checkbox patterns

**Key distinction**: Checkbox = deferred action (submit after selecting). Toggle = immediate action (effect on change).

**Checkbox variants by context**:
- **Multi-select group**: Multiple checkboxes with a submit button
  - Example: checkboxes for "Select invoices", then "Export" button
- **Single option with label**: Single checkbox for a feature/agreement
  - Example: "Subscribe to monthly statements" (one checkbox, one setting)
- **"Select all" pattern**: Master checkbox + item checkboxes
  - Use only when list is finite and manageable (≤20 items)
  - Example: in table, "Select all visible rows" master checkbox

**Behavior**:
- Checked = true, Unchecked = false, Indeterminate = some items in group selected
- Clicking checkbox toggles state immediately (visual feedback)
- But actual save/submission happens on form submit or explicit action
- Accessible: always has associated label (not placeholder text)

**Web vs Mobile**:
- Web: standard 16-20px checkbox, label on right
- Mobile: increase touch target to 44px (use `comfortArea` prop)
- Mobile: larger spacing between items in list

**Pairing**:
- Checkbox + Submit button = deferred multi-select
- Single checkbox = feature flag or agreement
- NOT: Checkbox + immediate onChange fire without submit

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

**For full API, props, variants, tokens**: See GitHub source above.
