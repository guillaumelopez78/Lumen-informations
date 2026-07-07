# Tabs - Guidelines

## Guidelines

Organises related content into switchable panels. Use when content sections are parallel and mutually exclusive.

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
