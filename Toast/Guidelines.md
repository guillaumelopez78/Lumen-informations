# Toast - Guidelines

## Toast Guidelines

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
| Action confirmation + optional "View" link | Persistent error → auto-dismiss before user can act |
| States what happened. Object + past-tense verb. Full stop. | Congratulatory tone is patronising for business software. Exclamation marks add noise. |
| Auto-dismiss after **5 seconds** — standard duration in Shine | Use durations under 3s or over 10s — 5s is the confirmed default |
| Display Toasts in the **bottom-right** corner of the screen | Place Toasts at the top or centered — bottom-right is the established position in Shine |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Auto-dismiss after 5 seconds on mobile — same duration as React | |
| Display Toast at the bottom of the screen on mobile | Place Toast at the top — bottom is the confirmed position |

---

---

### Imports

**Web**:
```tsx
import { Toast } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Toast } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { toast } from '@shinetools/lumen-react';

toast.success('Invoice sent', {
  action: { label: 'View', onClick: () => navigate('/invoices/123') }
});
toast.danger('Export failed — try again');
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Action confirmation + optional "View" link | Persistent error → auto-dismiss before user can act |
| States what happened. Object + past-tense verb. Full stop. | Congratulatory tone is patronising for business software. Exclamation marks add noise. |
| Auto-dismiss after **5 seconds** — standard duration in Shine | Use durations under 3s or over 10s — 5s is the confirmed default |
| Display Toasts in the **bottom-right** corner of the screen | Place Toasts at the top or centered — bottom-right is the established position in Shine |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Auto-dismiss after 5 seconds on mobile — same duration as React | |
| Display Toast at the bottom of the screen on mobile | Place Toast at the top — bottom is the confirmed position |

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Toast } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Toast } from '@shinetools/lumen-native';
```
