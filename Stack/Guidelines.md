# Stack - Guidelines

## Stack Guidelines

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
| `<XStack gap={8} align="center">` for icon + label rows | `<div style={{display:'flex',gap:'8px'}}>` — inline styles bypass token system |
| `<YStack gap={16}>` for form field stacking | Nest `<div>` with `flexDirection: column` manually |
| Compose stacks — `<YStack>` containing `<XStack>` items | Use one-off flex wrappers for every layout |

---

---

### Imports

**Web**:
```tsx
import { Stack (XStack / YStack) } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Stack (XStack / YStack) } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { XStack, YStack } from '@shinetools/lumen-react';

// Icon + label row
<XStack gap={8} align="center">
  <Icon icon={CheckCircle} size="small" />
  <Typography.Text>Payment confirmed</Typography.Text>
</XStack>

// Form field column
<YStack gap={16}>
  <TextField label="First name" />
  <TextField label="Last name" />
  <TextField label="Email" type="email" />
</YStack>

// Card layout
<YStack gap={12} padding={20}>
  <Typography.Header as="h3">Invoice #1042</Typography.Header>
  <XStack gap={8} justify="space-between">
    <Typography.Text variant="secondary">Total</Typography.Text>
    <Typography.Text weight="semibold">1 250,00 €</Typography.Text>
  </XStack>
</YStack>
```

---

---

## Do / Don't

| ✅ Do | ❌ Don't |
|---|---|
| `<XStack gap={8} align="center">` for icon + label rows | `<div style={{display:'flex',gap:'8px'}}>` — inline styles bypass token system |
| `<YStack gap={16}>` for form field stacking | Nest `<div>` with `flexDirection: column` manually |
| Compose stacks — `<YStack>` containing `<XStack>` items | Use one-off flex wrappers for every layout |

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Stack } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Stack } from '@shinetools/lumen-native';
```
