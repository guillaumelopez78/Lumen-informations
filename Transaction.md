---
name: Transaction
category: Data display
status: stable
---

# Transaction

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/transaction
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/transaction

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟡 WIP | — | Not yet released, coming soon |
| 📱 Mobile (lumen-native) | 🟡 WIP | — | Not yet released, coming soon |

**Recommendation**: Custom/internal pattern only. Transaction is vault-only at this time.

---

## Guidelines

A single transaction row — merchant, amount, date, and category. Used in transaction lists, account summaries, and card statements.

### Imports

**Web**:
```tsx
import { Transaction } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Transaction } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
<Transaction />
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
