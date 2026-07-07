# Alert - Guidelines

## Guidelines

**Use Alert when**: Persistent page-level messages that require user acknowledgment. Specifically:
- **Warning state** → "Account balance below €100" (user should act but can delay)
- **Blocking error** → "VAT number invalid — fix before submitting form" (requires action)
- **Info/context** → "This invoice is overdue" (informational, not blocking)
- **Action required** → "Payment method expired — update before checkout"
- **Page-level notices** → "Read-only mode" (affects entire page behavior)

**Don't use Alert when**:
- ❌ Temporary feedback → use Toast (auto-dismiss)
- ❌ System-wide messages → use Banner (full-width at top)
- ❌ Critical blocking action → use Dialog (hard stop to flow)
- ❌ Non-critical info → use inline text or help text on field

**Alert variants by severity**:
- `danger`: Blocking errors preventing progression. User must fix to continue.
  - "Invoice number invalid — use format INV-YYYY-XXXX"
  - "Payment failed — update payment method before retrying"
- `warning`: Action recommended but not blocking. User can acknowledge and continue.
  - "Balance low — consider topping up"
  - "This action has not been saved"
- `info`: Contextual information for user awareness.
  - "This customer has outstanding invoices"
  - "Bulk edit mode enabled"
- `success`: Rare. Confirmation of successful action. Usually Toast is better.

**Behavior**:
- Stays visible until dismissed (by user or automatic resolution)
- Includes action button when user can take immediate action
- Position: inline on page where context matters
- At top of section if page-level, or near affected field if field-level

**Layout context**:
- Inline Alert in form → above the problematic field or at form top
- Inline Alert in table → above the table to indicate bulk operation or data state
- Inline Alert in dashboard → above affected widget or at page top

**Web vs Mobile**: Same behavior. On mobile, alert takes full width and wraps text.

**Pairing with other components**:
- Alert (warning) + Toast (success after action) = full feedback loop
- Alert (danger) + Modal (confirmation of fix) = blocking flow
- Never use Alert + Toast for same issue (use one or the other)

### Imports

**Web**:
```tsx
import { Alert } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Alert } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
<Alert />
```

---

---

## Do / Don't

| ✅ Do | ❌ Don't |
|---|---|
| Use `danger` for blocking errors that prevent progression | Use `danger` for mild warnings |
| Include a resolution path (`action`) when applicable | Show an error with no way to fix it |
| Keep body copy concise | Write long paragraphs inside an Alert |

---
