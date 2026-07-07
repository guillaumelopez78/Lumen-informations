# Banner - Guidelines

## Banner Guidelines

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
| One banner, top of page — clear priority | 3 stacked banners — user can't tell what matters most |
| Place Banners above the page header, at the very top of the viewport — above everything else | Place a Banner below the header or inside a section — it belongs at the very top of the page |
| Use `warning` and `error` variants — these are the primary use cases for Banner in Shine | Use `success` for action confirmations — prefer a Toast for post-action success feedback |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Place Banner above the app header on mobile — sticky at the very top | Place Banner inside scroll content on mobile |

---

---

### Imports

**Web**:
```tsx
import { Banner } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Banner } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Banner } from '@shinetools/lumen-react';

// Variants
<Banner variant="success" message="Invoice sent successfully." />
<Banner variant="warning" message="Account balance below €100." />
<Banner variant="error" message="Payment failed — update your method." />

// With title and action
<Banner
  variant="warning"
  title="Balance low"
  message="Balance below €100."
  actionLabel="Top up"
  onAction={topUp}
/>
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| One banner, top of page — clear priority | 3 stacked banners — user can't tell what matters most |
| Place Banners above the page header, at the very top of the viewport — above everything else | Place a Banner below the header or inside a section — it belongs at the very top of the page |
| Use `warning` and `error` variants — these are the primary use cases for Banner in Shine | Use `success` for action confirmations — prefer a Toast for post-action success feedback |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Place Banner above the app header on mobile — sticky at the very top | Place Banner inside scroll content on mobile |

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Banner } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Banner } from '@shinetools/lumen-native';
```
