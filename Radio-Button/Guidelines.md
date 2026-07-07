# Radio-Button - Guidelines

## Guidelines

**Use RadioButton when**: Mutually exclusive (pick ONE) choice where **all options must be visible** for comparison. Specifically:
- **Billing frequency selection** → Monthly, Quarterly, Annual (3-4 options visible side-by-side)
- **Invoice template choice** → Standard, Minimalist, Professional (design templates, user compares visually)
- **Account type selection** → Personal, Business, Enterprise (during signup)
- **Feature flags with context** → "Auto-save: Always, On request, Never" (user sees all + descriptions)
- **Payment method selection** → Bank transfer, Card, SEPA (limited options, all visible)

**Don't use RadioButton when**:
- ❌ More than 5-6 options → use Select instead (dropdown keeps list compact)
- ❌ Options don't fit on screen → use Select instead
- ❌ Multi-select (pick many) → use Checkbox instead (radio is mutually-exclusive)
- ❌ Binary yes/no → use Toggle (simpler UI) or Checkbox (if part of form)
- ❌ Complex option descriptions → use custom card selection pattern instead

**Key rule**: RadioButton shows ALL options. If they don't all fit, switch to Select.

**RadioButton behavior**:
- Only ONE option selected at a time
- Clicking an unselected radio selects it (and deselects others)
- Label is clickable (not just the radio circle)
- Fieldset + legend wrap the group (semantic HTML)
- No submit delay — selection is the action itself (but submit may follow)

**When to show hints/descriptions**:
- Radio with short hint text below each option = good (helps comparison)
- Example: "Monthly: Flexible billing, pause anytime" vs "Annual: 20% discount, annual commitment"
- If hint text is long → use cards with radio instead, not basic radio

**Web vs Mobile**:
- Web: inline radio options if 3-4 fit in one row, otherwise stack vertically
- Mobile: always stack vertically (one radio per row) for touch targets
- Mobile: increase touch area with `comfortArea` prop

**Context by page**:
- Signup/onboarding → account type radio selection
- Billing settings → plan frequency (monthly/annual) selection
- Invoice editor → template/design selection
- Settings → preference selection (auto-save behavior, notification frequency)

**Pairing**:
- Radio group + "Save" button = select option, then confirm
- Radio group (standalone) = selection is the action (no submit needed)
- Radio + dependent fields = selecting one radio shows different fields below

### Imports

**Web**:
```tsx
import { RadioButton } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { RadioButton } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { RadioButton } from '@shinetools/lumen-react';

const [freq, setFreq] = useState('monthly');

<fieldset>
  <legend>Billing frequency</legend>
  <RadioButton label="Monthly" name="freq" value="monthly"
    checked={freq === 'monthly'} onChange={() => setFreq('monthly')} comfortArea />
  <RadioButton label="Quarterly" name="freq" value="quarterly"
    checked={freq === 'quarterly'} onChange={() => setFreq('quarterly')} comfortArea />
  <RadioButton label="Annual" name="freq" value="annual"
    checked={freq === 'annual'} onChange={() => setFreq('annual')} comfortArea />
</fieldset>
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| All options + hints visible — easy to compare | Select hides hint text — user can't compare |
| Switch to Select when the group exceeds 4–5 options — keep radio groups short so options fit without scrolling | Stack more than 5 radio options — switch to Select when list grows beyond 4–5 |

### Native (Mobile)


> 🔴 To define — Native RadioButton guidelines not yet documented.

---
