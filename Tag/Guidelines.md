# Tag - Guidelines

## Guidelines

**Use Tag when**: Displaying categories, filters, or metadata labels. Specifically:
- **Applied filters** → invoice status tags (Paid, Pending, Overdue) that can be cleared
- **Interactive category selector** → click tags to filter (selected = highlighted)
- **Metadata display** → "Internal Use Only", "Q4 2025", "Client XYZ" (read-only labels)
- **Skill/label chips** → team tags on customer profiles, invoice tags
- **Removable filter tags** → selected filters in toolbar with X to remove
- **Status chips** → non-changing status display (unlike Badge which is system state)

**Don't use Tag when**:
- ❌ System status indicators → use Badge instead (Paid, Draft, Sent states)
- ❌ Notification indicators → use Badge for count badges (5 new messages)
- ❌ Non-interactive labels → just use plain text or `<span>`
- ❌ Large group of tags (20+) → consider if all should be visible or searchable
- ❌ Icons and long text → Tag is for short, compact labels

**Key distinction**:
- **Tag** = user/system-defined category, often clickable/removable, for organizing data
- **Badge** = system-generated status indicator (not removable, represents state)
- **Chip** = tag variant with optional clear button, often in lists or filters

**Tag variants by context**:
- **Filter tags (removable)**: `onClear()` function provided
  - Example: `<Tag label="Invoice" onClear={() => clearFilter('invoice')} />`
  - Appears in toolbar after user selects filter
  - Visual feedback: highlighted when active
- **Interactive tags (selectable)**: `isSelected` + `onClick()`
  - Example: category selector showing "All", "Personal", "Business", "Freelance"
  - One tag can be selected (radio-like) or multiple (checkbox-like)
- **Static tags (read-only)**: no callbacks, just display
  - Example: "Q4 2025", "EUR", "Internal Use Only"
  - Scanning metadata without interaction

**Color/variants**:
- `color="blue"` → primary category or active filter
- `color="gray"` or `color="neutral"` → secondary categories
- `color="red"` → warning/caution categories (use sparingly)
- Sizes: `size="small"` (compact), `size="medium"` (default), `size="large"` (prominent in toolbars)

**Behavior**:
- Click tag → if `isSelected` or `onClick` provided, toggles state
- Click X (clear button) → fires `onClear()`, removes tag from view
- Tag can be selected or unselected (visual distinction)
- No destructive actions (tag is a filter/label, not a button)

**Web vs Mobile**:
- Web: inline tags in toolbar, flexible wrapping
- Mobile: single-row scrollable tags or wrap to multiple rows
- Mobile: larger touch targets (44px minimum height with `size="large"`)
- Mobile: clear button (X) more prominent on touch

**Pairing**:
- Tags + Table → filter table by selected tags
- Tags (removable) + Search → applied filters above search results
- Tags (interactive) + Drawer → select tags, then apply filters
- Multiple tags + Chip pattern → "Selected: Invoice, Paid, Q4" with clear buttons

**When to limit tag display**:
- Show 3-5 most-used tags first
- Add "Show more" if additional tags exist
- Searchable tag list if 10+ options

### Imports

**Web**:
```tsx
import { Tag } from '@shinetools/lumen-react';
```

**Mobile**:
```tsx
import { Tag } from '@shinetools/lumen-native';
```

### Basic Usage

```tsx
import { Tag, TagGroup } from '@shinetools/lumen-react';

// Applied filters (clearable)
<TagGroup>
  <Tag label="Invoice" color="blue" onClear={() => removeFilter('invoice')} />
  <Tag label="Q4 2025" color="neutral" onClear={() => removeFilter('q4')} />
</TagGroup>

// Interactive (selected state)
{categories.map(cat => (
  <Tag
    key={cat.id}
    label={cat.name}
    color="blue"
    isSelected={selected === cat.id}
    onClick={() => setSelected(cat.id)}
  />
))}
```

---

---

## Do / Don't

### React (Web)


| ✅ Do | ❌ Don't |
|---|---|
| Removable filter chips + interactive category selector | Tags as non-interactive status labels → use Badge |
| Use Tag for both interactive filtering (`isSelected`, `onClear`) and static metadata labels — both are valid in Shine | Force Tag into one role — filtering tags and metadata display tags coexist in the product |
| Use `size="large"` for filter tags in table toolbars — it's the standard size for table filters in Shine | Use `small` or `medium` for filter tags in tables — `large` is the confirmed default for this context |

### Native (Mobile)


> 🔴 To define — Native Tag guidelines not yet documented.

---
