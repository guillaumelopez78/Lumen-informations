# TextField - Guidelines

## TextField-Specific Guidelines

### Label & Placeholder Strategy
- **Label**: Always present, never float away (use visible label)
- **Placeholder**: Use for format example only ("YYYY-MM-DD")
- **Hint text**: Show constraints and format requirements
- **Caption**: Only for errors or real help text

### Validation Patterns
- Validate `onBlur` (after user leaves field)
- Show error message ONLY after blur
- Match error message to actual validation rule
- Give users actionable error text ("Enter 6 digits" not "Invalid")

### Input Types
- **Email**: Use `type="email"` for mobile keyboard
- **Phone**: Use `type="tel"` for numeric keyboard
- **Password**: Use `type="password"` with show/hide toggle
- **Search**: Use `type="search"` with clear button
- **Number**: Use `type="number"` with increment buttons

### State Management
- Pre-fill known values (first/last name, email)
- Show loading indicator for async validation
- Clear error when user starts typing
- Use `disabled` sparingly (show reason in hint)

### Accessibility
- Label associated with `htmlFor` attribute
- Error messages with `aria-describedby`
- Required fields marked with `*` AND `aria-required="true"`
- Hint text should enhance, not replace label


---

## Do / Don't

| ✅ Do | ❌ Don't |
|---|---|
| Always pair a field with a visible label | Use placeholder as the only label |
| Show error messages via `error` prop | Use colour alone to signal errors |
| Use `caption` for formatting guidance (e.g. "DD/MM/YYYY") | Show hints only after an error |
| Use `readOnly` for non-editable data | Disable fields that should just be viewable |

---

---

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


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { TextField } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { TextField } from '@shinetools/lumen-native';
```
