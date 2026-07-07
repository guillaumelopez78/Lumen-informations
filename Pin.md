---
name: Pin
category: Forms
status: stable
---

# Pin

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/pin
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/pin

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

---

## Guidelines

Segmented input for numeric codes — PINs, OTPs, verification codes. Focus auto-advances between segments.

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

**For full API, props, variants, tokens**: See GitHub source above.
