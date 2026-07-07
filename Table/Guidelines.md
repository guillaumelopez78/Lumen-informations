# Table - Guidelines

## Guidelines

Displays structured tabular data with sorting, selection, and actions. The primary data display component for B2B surfaces.

### Imports

**Web**:
```tsx
import { Table } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Table } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
type Column = {
  key: string; label: string;
  sortable?: boolean;
  align?: 'left' | 'center' | 'right';
  render?: (value, row) => ReactNode;
}
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Full amounts + semantic badge column | Truncated amount + icon-only actions (inaccessible) |
| Make all columns sortable by default — sorting is always on in Shine tables | Opt-in to sorting per column — all columns are sortable unless explicitly disabled |
| Use a full empty state (illustration + title + description + CTA) when the table has no results — it's the standard in Shine | Show a plain "No results" row or leave the table empty without context or action |

### Native (Mobile)


> 🔴 To define — Native Table guidelines not yet documented.

---
