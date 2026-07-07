---
name: Card
category: Data display
status: stable
---

# Card

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/card
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/card

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟡 WIP | — | Not yet released, coming soon |
| 📱 Mobile (lumen-native) | 🟡 WIP | — | Not yet released, coming soon |

**Recommendation**: Custom implementation needed. Use basic styled containers with Divider + Typography + other primitives.

---

## Guidelines

**Use Card when**: Displaying grouped information in dashboard/summary contexts. Lumen has 6 card types, each for specific data:

**Card.Number**: Key metrics on dashboards/analytics pages
- In **dashboard** → total revenue, invoice count, payment success rate
- In **analytics** → trend metrics with % change vs previous period
- In **financial summary** → outstanding balance, average invoice value
- Example: "€12,450 total invoiced (+8% vs last month)"

**Card.Status**: Current state/count of business entity
- In **invoice list header** → pending, sent, paid invoice counts
- In **dashboard widgets** → active subscriptions, team members, integrations
- Example: "15 pending invoices"

**Other Card variants**: Check source code for Invoice, Payment, Transaction, Customer cards

**Don't use Card when**:
- ❌ Displaying lists with many items → use Table component
- ❌ Detailed drill-down data → use expanded page view, not card
- ❌ Simple text blocks → use plain text or Alert/Banner
- ❌ Comparing 10+ data points → use Chart component instead

**Context matters**: Cards are for scanning metrics at a glance. Not for detailed transactions (use Table).

**Web vs Mobile**: Cards are responsive. On mobile, stack vertically in single column. Desktop can show 2-3 cards per row.

### Imports

**Web**:
```tsx
import { Card } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Card } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
<Card.Number
  label="Total invoiced"
  value="€ 12 450"
  trend={{ direction: 'up', value: '+8%', label: 'vs last month' }}
/>
```

---

## Do / Don't

### React (Web)

| ✅ Do | ❌ Don't |
|---|---|
| [Good practice] | [Bad practice] |
| [Good practice] | [Bad practice] |

### Native (Mobile)

| ✅ Do | ❌ Don't |
|---|---|
| [Good practice] | [Bad practice] |
| [Good practice] | [Bad practice] |

---

**For full API, props, variants, tokens**: See GitHub source above.
