# Select - Guidelines

## Guidelines

Dropdown for choosing a single option from a predefined list. Use when list has more than 5 options — prefer Radio for fewer.

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
