# Select - Guidelines

## Select-Specific Guidelines

### Option Count Rules
- **2-4 options**: Use RadioButton (all visible at once)
- **5-10 options**: Use Select (dropdown to avoid clutter)
- **10+ options**: Consider searchable Select or Autocomplete

### Placeholder & Defaults
- Placeholder describes what to choose: "Choose a country"
- Placeholder "Select" alone is too vague
- Pre-select common default to reduce friction
- Empty placeholder only if conscious choice is required

### Option Labeling
- Use short noun phrases: "High priority", "Draft", "Published"
- Avoid verbs or questions
- Group related options with `<optgroup>`
- Show icon/badge for status options (color-blind safe)

### Search in Select
- Show search field if 8+ options
- Search filters by text match
- Highlight matched text in results
- Show "No results" when no match

### Accessibility
- Label associated with `<select>`
- Option descriptions if complex
- Keyboard navigation: Arrow keys to browse
- Mobile: Native picker on iOS/Android

### When NOT to Use
- Single on/off: Use Switch instead
- Multi-select: Use Checkbox group instead
- Instant search: Use Autocomplete instead


---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Select for 5+ options — comparison not needed | 2 options in a Select — Radio shows both at once |
| Use Select even for long lists (20+ options) — it's the standard pattern in Shine regardless of list size | Switch to Autocomplete based on list length alone — only use Autocomplete when search is genuinely needed |
| Rely on the placeholder for filter Selects ("Select a status…") — no global convention for a "All" option yet | Add a "All" or "None" option by default — no cross-team convention defined yet, align per-feature |

### Native (Mobile)


> 🔴 To define — Native Select guidelines not yet documented.

---

---

### Imports

**Web**:
```tsx
import { Select } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Select } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Select } from '@shinetools/lumen-react';

const options = [
  { value: 'card', label: 'Credit card' },
  { value: 'transfer', label: 'Bank transfer' },
];

// Basic usage
<Select
  label="Payment method"
  options={options}
  value={method}
  onChange={setMethod}
/>

// With error + caption
<Select
  label="Country"
  options={countries}
  placeholder="Choose a country…"
  value={country}
  onChange={setCountry}
  error="Required"
/>
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Select for 5+ options — comparison not needed | 2 options in a Select — Radio shows both at once |
| Use Select even for long lists (20+ options) — it's the standard pattern in Shine regardless of list size | Switch to Autocomplete based on list length alone — only use Autocomplete when search is genuinely needed |
| Rely on the placeholder for filter Selects ("Select a status…") — no global convention for a "All" option yet | Add a "All" or "None" option by default — no cross-team convention defined yet, align per-feature |

### Native (Mobile)


> 🔴 To define — Native Select guidelines not yet documented.

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Select } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Select } from '@shinetools/lumen-native';
```
