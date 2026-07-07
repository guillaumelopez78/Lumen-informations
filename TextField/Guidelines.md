# TextField - Guidelines

## Guidelines

**Use TextField when**: Collecting single-line text input. Specifically:
- In **signup/login flows** → email address, password, name
- In **checkout** → recipient name, street address, zip code, phone
- In **invoice management** → invoice number, VAT ID, customer name
- In **search/filtering** → search queries (or use Search component for autocomplete)
- In **profile editing** → company name, phone number, website URL

**Don't use TextField when**:
- Multiple lines needed → use TextArea
- Predefined options exist → use Select, Autocomplete, RadioButton, or Checkbox
- Yes/No choice → use Toggle or Checkbox
- Date/time input → use DatePicker (not a text field)
- Phone numbers with country selection → use Input.PhoneNumber component
- Numbers with currency → use currency-formatted input with proper decimal handling

**Web vs Mobile**: TextField adapts automatically. On mobile, numeric keyboard appears for `type="number"`, email keyboard for `type="email"`, which improves input speed.

**When NOT to use**:
- ❌ Multi-line text → use TextArea
- ❌ Predefined choices → use Select, Autocomplete, or Radio
- ❌ Yes/No setting → use Toggle
- ❌ Date input → use DatePicker

### Imports

**Web**:
```tsx
import { Input } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Input } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { TextField } from '@lumen/react';
import { Mail } from 'lucide-react';

// Default
<TextField
  label="Email address"
  type="email"
  placeholder="you@company.com"
  caption="We'll send your invoice here"
  required
/>

// Error state
<TextField
  label="VAT number"
  value={vatNumber}
  onChange={(e) => setVatNumber(e.target.value)}
  error="Invalid VAT format — expected FR followed by 11 digits"
/>

// With icons
<TextField
  label="Search"
  startIcon={<Mail size={16} />}
  placeholder="Search invoices…"
/>

// Subtle variant
<TextField
  label="Amount"
  variant="subtle"
  type="number"
  size="sm"
/>
```

---

---

## Do / Don't

| ✅ Do | ❌ Don't |
|---|---|
| Always pair a field with a visible label | Use placeholder as the only label |
| Show error messages via `error` prop | Use colour alone to signal errors |
| Use `caption` for formatting guidance (e.g. "DD/MM/YYYY") | Show hints only after an error |
| Use `readOnly` for non-editable data | Disable fields that should just be viewable |

---
