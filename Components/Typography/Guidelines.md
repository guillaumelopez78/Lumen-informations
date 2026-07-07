# Typography - Guidelines

## Typography Guidelines

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

| ✅ Do | ❌ Don't |
|---|---|
| Use `Typography.Header as="h2"` for section titles — semantic structure | Use `Typography.Text weight="semibold"` to visually fake a heading |
| Use `variant="secondary"` for supporting/metadata text | Override token colors with inline styles |
| Match `size` on `Typography.Link` to surrounding `Typography.Text` size | Use a link size that doesn't match surrounding body text |

---

---

### Imports

**Web**:
```tsx
import { Typography } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Typography } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Typography } from '@shinetools/lumen-react';

// Headers
<Typography.Header as="h1">Invoices</Typography.Header>
<Typography.Header as="h2">Recent activity</Typography.Header>
<Typography.Header as="display">Send money, simply.</Typography.Header>

// Body text
<Typography.Text>Default body copy.</Typography.Text>
<Typography.Text variant="secondary" size="small">Created on 12 Jan 2026</Typography.Text>
<Typography.Text weight="semibold">Invoice total</Typography.Text>

// Inline link
<Typography.Link href="/invoices">View all invoices</Typography.Link>
<Typography.Link href="/help" size="small">Learn more</Typography.Link>
```

---

---

## Do / Don't

| ✅ Do | ❌ Don't |
|---|---|
| Use `Typography.Header as="h2"` for section titles — semantic structure | Use `Typography.Text weight="semibold"` to visually fake a heading |
| Use `variant="secondary"` for supporting/metadata text | Override token colors with inline styles |
| Match `size` on `Typography.Link` to surrounding `Typography.Text` size | Use a link size that doesn't match surrounding body text |

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Typography } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Typography } from '@shinetools/lumen-native';
```
