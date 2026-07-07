# Switch - Guidelines

## Switch-Specific Guidelines

### Core Pattern
- **Immediate effect**: Setting takes effect instantly
- **No save button**: Toggle alone is the complete action
- **Stateful**: Reflects current on/off state
- **Accessible**: Must announce state to screen readers

### When to Use Switch
- Notification preferences (instant on/off)
- Feature toggles and flags
- Permission grants (access control)
- Settings with immediate effect

### When NOT to Use Switch
- Form-based selection: Use Checkbox instead
- Multi-select filtering: Use Checkbox instead
- Delayed saves: Use Checkbox + submit button instead

### Label Best Practices
- Describe what is being enabled: "Invoice reminders", "2FA"
- Avoid generic labels: "Enable" alone is unclear
- Use status-positive language: "Notifications" not "Don't notify"
- Keep labels short and scannable

### Context & Placement
- **Permissions**: Primary pattern in Shine
- **Settings lists**: Use `size="compact"` for density
- **Feature toggles**: Show in feature cards
- **Dashboard**: Top-level on/off controls

### Feedback
- Immediate visual feedback (toggle animates)
- Show confirmation if irreversible
- Toast/dialog for significant changes
- History/audit log for access changes


---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Descriptive labels — user knows exactly what each toggle controls | "Enable" and "Toggle" — no context for the user |
| Apply changes immediately on toggle — never require a Save button after flipping a Switch | Put a Switch inside a form with a Submit button — use Checkbox for form-based multi-select |
| Use Switch to activate/deactivate collaborator access or permissions — it's the main pattern in Shine for rights management | Show a confirmation modal before applying a Switch toggle — the action should be instantaneous |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Apply changes immediately on toggle, same as React | Require a Save button after toggling a Switch on mobile |
| Use Switch for permissions and access rights on mobile — same pattern as React | |

---

---

### Imports

**Web**:
```tsx
import { Switch } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Switch } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Switch } from '@shinetools/lumen-react';

// Basic usage
<Switch
  aria-label="Email notifications"
  checked={notifications}
  onCheckedChange={setNotifications}
/>

// Sizes
<Switch aria-label="Push notifications" size="large" checked={push} onCheckedChange={setPush} />
<Switch aria-label="Dark mode" size="compact" checked={dark} onCheckedChange={setDark} />
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Descriptive labels — user knows exactly what each toggle controls | "Enable" and "Toggle" — no context for the user |
| Apply changes immediately on toggle — never require a Save button after flipping a Switch | Put a Switch inside a form with a Submit button — use Checkbox for form-based multi-select |
| Use Switch to activate/deactivate collaborator access or permissions — it's the main pattern in Shine for rights management | Show a confirmation modal before applying a Switch toggle — the action should be instantaneous |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Apply changes immediately on toggle, same as React | Require a Save button after toggling a Switch on mobile |
| Use Switch for permissions and access rights on mobile — same pattern as React | |

---


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Switch } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Switch } from '@shinetools/lumen-native';
```
