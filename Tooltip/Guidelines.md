# Tooltip - Guidelines

## Guidelines

Short contextual label on hover/focus. For supplementary info only — never essential content that touch users cannot access. Uses `@floating-ui/react` for positioning.

### Imports

**Web**:
```tsx
import { Tooltip } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Tooltip } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Tooltip } from '@shinetools/lumen-react';
import { Button, Icon } from '@shinetools/lumen-react';
import { Download } from 'lucide-react';

// Icon-only button
<Tooltip label="Export as CSV">
  <Button variant="text" aria-label="Export" startIcon={<Icon icon={Download} />} />
</Tooltip>

// Custom placement & no pointer
<Tooltip label="Copied!" placement="bottom" showPointer={false}>
  <button>Copy IBAN</button>
</Tooltip>

// Controlled
<Tooltip label="Saved" open={showSaved} onOpenChange={setShowSaved}>
  <Button variant="text">Save</Button>
</Tooltip>
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Add Tooltip to icon-only buttons — `label` provides the context screen readers need | Duplicate a visible label in a Tooltip — no value added |
| Use on truncated text (ellipsis) to reveal the full value | Put a Tooltip on every UI element — creates noise |
| Keep `delay` at 700ms (default) to avoid flickering on cursor movement | Set `delay={0}` — causes intrusive popups on mouse pass-through |
| Use `placement="bottom"` when the trigger is near the top of the viewport | Always use `placement="top"` — it may clip against the window edge |

### Native (Mobile)


> Tooltip is hover-only. On mobile, expose the label as an `accessibilityLabel` on the trigger instead.

---
