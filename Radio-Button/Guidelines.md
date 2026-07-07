# Radio-Button - Guidelines

## Radio-Button Guidelines

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
| All options + hints visible — easy to compare | Select hides hint text — user can't compare |
| Switch to Select when the group exceeds 4–5 options — keep radio groups short so options fit without scrolling | Stack more than 5 radio options — switch to Select when list grows beyond 4–5 |

### Native (Mobile)


> 🔴 To define — Native RadioButton guidelines not yet documented.

---

---

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


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Radio-Button } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Radio-Button } from '@shinetools/lumen-native';
```
