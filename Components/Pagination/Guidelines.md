# Pagination - Guidelines

## Pagination Guidelines

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
| "1–20 of 834" + ellipsis — navigates any dataset | All 22 pages rendered — breaks at 50+ pages |
| Use numbered pagination (always page numbers, never infinite scroll) — the only pagination pattern in Shine | Use infinite scroll or a "Load more" button — Shine uses numbered pages exclusively |
| Hide the Pagination component when there is only 1 page — show it only when there are 2 or more pages | Always show Pagination regardless of total pages — it's meaningless with a single page |
| Let the user choose their page size — a page size selector is part of the Pagination pattern in Shine | Force a fixed page size — the user should be able to control how many items they see |

### Native (Mobile)


| ✅ Do | ❌ Don't |
|---|---|
| Use numbered pagination on mobile — hide when only 1 page | Use infinite scroll on mobile — numbered pages is the only pattern |

---

---

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


### Implementation Pattern
- Import from `@shinetools/lumen-react` or `@shinetools/lumen-native`
- Follow component API from source
- Use design tokens for colors and spacing
- Test in isolation, then in context

### Imports

**Web**:
```tsx
import { Pagination } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Pagination } from '@shinetools/lumen-native';
```
