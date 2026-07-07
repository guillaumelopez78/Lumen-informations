---
name: Search
category: Forms
status: stable
---

# Search

**Source Code**:
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react/src/lib/search
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native/src/lib/search

---

## Status & Availability

| Platform | Status | Version | Notes |
|----------|--------|---------|-------|
| 🌐 Web (lumen-react) | 🟡 WIP | — | Not yet released, coming soon |
| 📱 Mobile (lumen-native) | 🟡 WIP | — | Not yet released, coming soon |

**Recommendation**: Use [[TextField]] with Icon pattern. Search is vault-only at this time.

---

## Guidelines

**Use Search when**: Filtering/searching content with optional autocomplete. Specifically:
- **Invoice list filtering** → search by invoice number, customer name, date range
- **Dashboard search** → find transactions, customers, documents across pages
- **Lightweight autocomplete** → search + show suggestions as user types
- **Filtering tables/lists** → search within visible data (not global search)
- **Not full-text search** → use Search component for scoped filtering, not app-wide search

**Don't use Search when**:
- ❌ Simple single-line input → use TextField (Search adds search icon + clear button)
- ❌ Predefined options only → use Select or Autocomplete instead
- ❌ Full-app/global search → use dedicated SearchPage component
- ❌ No filtering needed → use plain TextField

**Search composition**:
- Search = TextField + search icon prefix + clear button suffix
- Built from Input component internally
- Placeholder: "Search invoices…" (specific context)
- Single-line input only (multi-line search doesn't exist)

**Behavior differences from TextField**:
- Clear button (X) appears automatically when user types
- Search icon shows intent (magnifying glass)
- Focuses on finding/filtering, not data entry
- Real-time filtering (as user types) vs form submission

**Web vs Mobile**:
- Web: search icon on left, clear button on right, inline in toolbar
- Mobile: full-width search at top of page/section, same icon/clear pattern
- On mobile, keyboard is search-optimized (numeric/text as needed)

**When to pair**:
- Search + Table → filter table rows
- Search + List → filter list items
- Search + Autocomplete → show suggestions + clear filtered results

### Imports

**Web**:
```tsx
import { Search } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Search } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
<Search />
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
