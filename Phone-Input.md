---
name: Phone-Input
category: Forms
status: stable
---

# Phone-Input

**Source Code**:
- 🌐 **Web (lumen-react)**: Not in repository
- 📱 **Mobile (lumen-native)**: Not in repository

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟡 WIP | — | Not yet released, coming soon |
| 📱 Mobile (lumen-native) | 🟡 WIP | — | Not yet released, coming soon |

**Recommendation**: Use [[TextField]] with validation instead. Input Phone Number is vault-only at this time.

---

## Guidelines

**Use Input.PhoneNumber when**: Collecting international phone numbers with country code. Specifically:
- **Signup/registration** → collect user phone number (may include country code)
- **Customer contact form** → phone field with international support
- **Billing/shipping** → contact phone in checkout or profile
- **Support/callback** → phone number for support requests
- **Invoice recipient** → contact phone on customer info
- **Two-factor auth** → phone number for SMS verification

**Don't use Input.PhoneNumber when**:
- ❌ Phone number with fixed country → use TextField with `type="tel"` instead
- ❌ Domestic phone numbers only → use TextField or numeric Input
- ❌ Optional field (rarely used) → use TextField
- ❌ No country selection needed → use TextField + country dropdown separate

**How it works**:
- Dropdown prefix showing country flag + country code (e.g., "+33 FR")
- User can search/select country from dropdown
- Text input shows remaining digits (auto-formats based on country)
- Example: Select France (+33), type "698765432" → stores "+33698765432"

**Behavior**:
- Country dropdown on left, phone number field on right
- Country defaults to user's locale (browser language) if available
- Auto-formats based on selected country (different countries have different formats)
- Validates international phone format (optional on your component)
- Returns full phone number with country code

**Context by page**:
- **Signup form** → phone field (optional or required) with country selector
- **Checkout** → billing/shipping phone with country code
- **Profile/settings** → user contact phone number
- **Customer creation** → phone field with country code (business customer)
- **API integrations** → phone field for webhook callbacks

**Web vs Mobile**:
- Web: country dropdown + text field side-by-side, comfortable spacing
- Mobile: country dropdown stacked above or full-height above phone field
- Mobile: phone keyboard appears when typing (tel input type)
- Mobile: country search might be search + dropdown or native select

**Validation**:
- Required/optional based on form context
- Client-side: check format matches selected country
- Server-side: validate international phone format
- Example error: "Invalid phone format for selected country"

**Pairing**:
- Phone input + Email → both contact methods in form
- Phone input + Country dropdown (separate) → if you need just country selection
- Phone input + SMS verification → 2FA or confirm phone number flow

**When to use vs TextField**:
- Input.PhoneNumber → international/multi-country app
- TextField `type="tel"` → single country or optional phone
- Input.PhoneNumber → business app (Shine supports international)
- TextField → consumer app with fixed locale

### Imports

**Web**:
```tsx
import { Input Phone Number } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Input Phone Number } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
<Input Phone Number />
```

---

## Do / Don't

### React (Web)

| ✅ Do | ❌ Don't |
|---|---|
| [Good practice] | [Bad practice] |
| [Good practice] | [Bad practice] |

### Native (Mobile)

| ✅ Do | ❌ Don't |
|---|---|
| [Good practice] | [Bad practice] |
| [Good practice] | [Bad practice] |

---

**For full API, props, variants, tokens**: See GitHub source above.
