---
name: Pagination
category: Navigation
status: stable
---

# Pagination

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/pagination
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/pagination

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟢 Stable | v0.0.1 | Production-ready |
| 📱 Mobile (lumen-native) | 🟡 WIP | — | Use scroll/load-more pattern instead |

---

## Guidelines

Controls for navigating between pages of content. Used at the bottom of Table and list views.

### Imports

**Web**:
```tsx
import { Pagination } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Pagination } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Pagination } from '@shinetools/lumen-react';

<Pagination
  page={page} totalPages={42} totalItems={834}
  pageSize={20} onChange={setPage}
/>
```

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| "1–20 of 834" + ellipsis — navigates any dataset | All 22 pages rendered — breaks at 50+ pages |
| Use numbered pagination (always page numbers, never infinite scroll) — the only pagination pattern in Shine | Use infinite scroll or a "Load more" button — Shine uses numbered pages exclusively |
| Hide the Pagination component when there is only 1 page — show it only when there are 2 or more pages | Always show Pagination regardless of total pages — it's meaningless with a single page |
| Let the user choose their page size — a page size selector is part of the Pagination pattern in Shine | Force a fixed page size — the user should be able to control how many items they see |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Use numbered pagination on mobile — hide when only 1 page | Use infinite scroll on mobile — numbered pages is the only pattern |

---

**For full API, props, variants, tokens**: See GitHub source above.
