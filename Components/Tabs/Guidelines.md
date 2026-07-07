# Tabs - Guidelines

## Tabs Guidelines

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
| 3 short labels + badge counter — scannable | 7 long labels — wraps and loses hierarchy |
| Use Tabs primarily in Settings pages — that's the most common context in Shine today | Force a fixed limit on tab count — no global cap is defined, let content drive the number |
| Keep tab labels short and parallel — all nouns or all verbs, never mixed | Mix label styles in one tab bar — creates uneven visual rhythm |

### Native (Mobile)


> 🔴 To define — Native Tabs guidelines not yet documented.

---

---

### Imports

**Web**:
```tsx
import { Tabs } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Tabs } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Tabs, Tab } from '@shinetools/lumen-react';

<Tabs value={active} onChange={setActive}>
  <Tab value="all" label="All" />
  <Tab value="income" label="Income" badge={12} />
</Tabs>
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| 3 short labels + badge counter — scannable | 7 long labels — wraps and loses hierarchy |
| Use Tabs primarily in Settings pages — that's the most common context in Shine today | Force a fixed limit on tab count — no global cap is defined, let content drive the number |
| Keep tab labels short and parallel — all nouns or all verbs, never mixed | Mix label styles in one tab bar — creates uneven visual rhythm |

### Native (Mobile)


> 🔴 To define — Native Tabs guidelines not yet documented.

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Tabs } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Tabs } from '@shinetools/lumen-native';
```
