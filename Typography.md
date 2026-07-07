---
name: Typography
category: Foundation
status: stable
---

# Typography

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/typography
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/typography

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟢 Stable | v0.0.1 | Production-ready |

---

## Guidelines

Semantic text components. Three sub-components cover all text needs: `Typography.Text` for body copy, `Typography.Header` for headings, `Typography.Link` for inline links. All use **Inter** exclusively.

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

## Do / Don't

| ✅ Do | ❌ Don't |
|---|---|
| Use `Typography.Header as="h2"` for section titles — semantic structure | Use `Typography.Text weight="semibold"` to visually fake a heading |
| Use `variant="secondary"` for supporting/metadata text | Override token colors with inline styles |
| Match `size` on `Typography.Link` to surrounding `Typography.Text` size | Use a link size that doesn't match surrounding body text |

---

**For full API, props, variants, tokens**: See GitHub source above.
