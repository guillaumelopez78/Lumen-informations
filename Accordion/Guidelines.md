# Accordion - Guidelines

## Guidelines

**Use Accordion when**: Progressive disclosure of grouped content. Specifically:
- **FAQ/help sections** → expandable Q&A on help page or support site
- **Settings panels** → group related settings (Account, Notifications, Billing, Security)
- **Transaction/invoice details** → expandable sections for line items, notes, attachments
- **Collapsible documentation** → technical details, advanced options, code examples
- **Form sections** → group related form fields (Billing address, Shipping address)
- **Dense content with hierarchy** → reduce page scrolling by collapsing non-essential sections

**Don't use Accordion when**:
- ❌ All content equally important → don't hide if users need everything visible
- ❌ Deeply nested accordions → max 1 level deep (accordion inside accordion confuses)
- ❌ Single expandable section → use Disclosure or plain collapsible div instead
- ❌ Required reading → if users must see it, don't hide in accordion
- ❌ Rare scenarios → if <10% of users expand a section, rethink the content

**Accordion patterns in Shine**:
- **Multiple sections open simultaneously** → default behavior, users expand as needed
- **All sections collapsed by default** → except the first section (defaultOpen)
- **With dividers** → visually separate sections (`showDivider` prop)
- **Without dividers** → more compact, for simpler hierarchies

**Context by page**:
- **Settings page** → Account (always open), Notifications, Billing, Security (all collapsible)
- **Invoice detail** → Summary (open), Line items (collapsible), Notes (collapsible), Attachments (collapsible)
- **Help/FAQ** → "How do I export data?" (expandable), "What payment methods?", "Why is my balance X?" (all collapsible)
- **Form (onboarding)** → Company info (open), Billing address, Shipping address (collapsible)

**Behavior**:
- Click header to toggle open/closed
- Multiple sections can be open at once (no exclusive mode)
- Smooth expand/collapse animation (300ms)
- No nested accordions (use flat structure with proper headings)
- Content inside can be anything: text, form fields, images, tables

**Accessibility**:
- Header is a clickable button with aria-expanded state
- Keyboard: Tab to focus, Space/Enter to toggle
- Screen reader announces expanded/collapsed state

**Web vs Mobile**:
- Web: accordions in 1-2 column layouts, side-by-side if needed
- Mobile: always single column, full-width
- Touch targets on mobile: 44px minimum height for header

**When NOT to hide content**:
- Critical information (required form fields) → show in form, not accordion
- High-frequency settings → don't accordion if >50% of users need it
- First-time users → first section open, rest closed (defaultOpen)

### Imports

**Web**:
```tsx
import { Accordion } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Accordion } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Accordion } from '@shinetools/lumen-react';

// Basic usage
<Accordion title="What is Shine?" defaultOpen>
  Shine is a business account for French SMEs and freelancers.
</Accordion>
<Accordion title="How do I export transactions?">
  Go to Transactions → Export → CSV or PDF.
</Accordion>

// With divider
<Accordion title="General" showDivider>...content...</Accordion>
<Accordion title="Notifications" showDivider>...content...</Accordion>
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| 2 items — first open, second ready to expand | Accordion inside accordion — depth 2 is confusing |
| Allow multiple panels to be open simultaneously — users can expand as many sections as they need | Force exclusive mode (one open at a time) — Shine lets users open multiple panels freely |
| Use Accordion for FAQ/help content, settings sections, and transaction details — all three are valid contexts in the product | Limit Accordion to a single use case — it's a versatile pattern in Shine |

### Native (Mobile)


> 🔴 To define — Native Accordion guidelines not yet documented.

---
