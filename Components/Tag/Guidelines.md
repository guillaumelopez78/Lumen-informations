# Tag - Guidelines

## Tag Guidelines

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
| Removable filter chips + interactive category selector | Tags as non-interactive status labels → use Badge |
| Use Tag for both interactive filtering (`isSelected`, `onClear`) and static metadata labels — both are valid in Shine | Force Tag into one role — filtering tags and metadata display tags coexist in the product |
| Use `size="large"` for filter tags in table toolbars — it's the standard size for table filters in Shine | Use `small` or `medium` for filter tags in tables — `large` is the confirmed default for this context |

### Native (Mobile)


> 🔴 To define — Native Tag guidelines not yet documented.

---

---

### Imports

**Web**:
```tsx
import { Tag } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Tag } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Tag, TagGroup } from '@shinetools/lumen-react';

// Applied filters (clearable)
<TagGroup>
  <Tag label="Invoice" color="blue" onClear={() => removeFilter('invoice')} />
  <Tag label="Q4 2025" color="neutral" onClear={() => removeFilter('q4')} />
</TagGroup>

// Interactive (selected state)
{categories.map(cat => (
  <Tag
    key={cat.id}
    label={cat.name}
    color="blue"
    isSelected={selected === cat.id}
    onClick={() => setSelected(cat.id)}
  />
))}
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Removable filter chips + interactive category selector | Tags as non-interactive status labels → use Badge |
| Use Tag for both interactive filtering (`isSelected`, `onClear`) and static metadata labels — both are valid in Shine | Force Tag into one role — filtering tags and metadata display tags coexist in the product |
| Use `size="large"` for filter tags in table toolbars — it's the standard size for table filters in Shine | Use `small` or `medium` for filter tags in tables — `large` is the confirmed default for this context |

### Native (Mobile)


> 🔴 To define — Native Tag guidelines not yet documented.

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Tag } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Tag } from '@shinetools/lumen-native';
```
