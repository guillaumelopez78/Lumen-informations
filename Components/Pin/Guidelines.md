# Pin - Guidelines

## Pin Guidelines

### Use Cases
- Primary use case 1
- Primary use case 2
- Primary use case 3
- Primary use case 4

### Best Practices
- Practice 1
- Practice 2
- Practice 3

### Accessibility Requirements
- Follow WCAG AA standards
- Test with screen readers
- Keyboard navigation support required
- Color must not be the only conveyor of meaning


---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| 6 segments — focus auto-advances, paste fills all | Single input — no guidance on position or progress |
| Use Pin for OTP (SMS/email, 6 digits) and app login PIN (4 digits) — these are the two confirmed use cases in Shine | Use Pin for other numeric inputs (amounts, account numbers) — it's specifically for codes with fixed lengths |
| Set `mask={false}` for OTP codes — users should see the code they received | Mask all codes — only use `mask={true}` for sensitive PINs (app login, security codes) |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| OTP (6 digits, unmasked) and app login PIN (4 digits, masked) — same as React | Use Pin for other numeric inputs |

---

---

### Imports

**Web**:
```tsx
import { Pin } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Pin } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Pin } from '@shinetools/lumen-react';

// OTP verification
<Pin
  label="Verification code"
  length={6}
  autoFocus
  onComplete={(code) => verifyOTP(code)}
/>

// Masked PIN entry
<Pin
  label="PIN"
  length={4}
  mask
  value={pin}
  onChange={setPin}
  error="Incorrect PIN, 2 attempts remaining"
/>
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| 6 segments — focus auto-advances, paste fills all | Single input — no guidance on position or progress |
| Use Pin for OTP (SMS/email, 6 digits) and app login PIN (4 digits) — these are the two confirmed use cases in Shine | Use Pin for other numeric inputs (amounts, account numbers) — it's specifically for codes with fixed lengths |
| Set `mask={false}` for OTP codes — users should see the code they received | Mask all codes — only use `mask={true}` for sensitive PINs (app login, security codes) |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| OTP (6 digits, unmasked) and app login PIN (4 digits, masked) — same as React | Use Pin for other numeric inputs |

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Pin } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Pin } from '@shinetools/lumen-native';
```
