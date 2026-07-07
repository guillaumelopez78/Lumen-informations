# Lumen Component Specifications

Complete, professional documentation for the Lumen design system components.

## 📁 Repository Structure

```
Lumen-component-specs/
├── Components/
│   ├── Accordion/
│   │   ├── Overview.md       # What & when to use
│   │   ├── Guidelines.md     # Best practices & do/don'ts
│   │   └── Specs.md          # Design tokens & props
│   ├── Alert/
│   ├── Button/
│   ├── ... (48 components total)
│   └── Typography/
├── README.md                  # This file
└── .github/                   # GitHub configuration
```

## 📖 Each Component Has 3 Files

### **Overview.md**
- **Purpose** — What the component is and why it exists
- **When to use** — Specific use cases (4-5 examples)
- **When NOT to use** — Anti-patterns to avoid
- **Source Code links** — Web (React) & Mobile (Native)
- **Status & Availability** — Platform support table

### **Guidelines.md**
Comprehensive best practices based on Material Design, Apple HIG, and Figma standards:

- **Component-Specific Guidelines**
  - Hierarchy & Context (where to use in UI)
  - Label Best Practices (microcopy)
  - Layout Patterns (form, modal, toolbar, mobile)
  - Accessibility Requirements (WCAG AA)
  - Async & Loading Patterns

- **Do / Don't Tables**
  - Numbered pairs with explanations
  - Separate React Web & Native Mobile guidelines
  
- **Implementation**
  - Import statements
  - Basic code examples

### **Specs.md**
Technical reference and design tokens:

- **Design Token System**
  - Colors (primary, accent, danger, neutral)
  - Typography (font, sizes, weights, line-height)
  - Spacing (padding, margin, gap)
  - Sizing (20px → 44px touch targets)
  - Motion (fast/standard/slow transitions)

- **Tokens Used** — Detailed table showing Property | Token | Value

- **Component Props**
  - Common props
  - Web-specific (React)
  - Mobile-specific (Native)

- **Variants**
  - Visual variants (filled, outlined, text, tonal)
  - State variants (default, hover, active, focus, disabled, loading)
  - Size variants (small, medium, large)

- **Related Components** — Cross-references
- **Browser & Device Support** — Compatibility matrix

---

## 🔗 Quick Links

**Source Code:**
- 🌐 **Web (lumen-react)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react
- 📱 **Mobile (lumen-native)**: https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native

**Documentation Standards:**
- Based on Material Design 3
- Follows Apple HIG conventions
- Uses Figma design system patterns
- Inspired by AI-ready design system

---

## ✨ 48 Components

### Forms & Input
- Button
- TextField
- Checkbox
- Radio-Button
- Switch
- Select
- Multi-Select
- Autocomplete
- Date-Picker
- Period-Picker
- Phone-Input
- Pin
- TextArea

### Feedback & Status
- Alert
- Toast
- Banner
- System-Banner
- Callout
- Progress
- Loader

### Data Display
- Card
- Table
- Pagination
- Badge
- Tag
- Avatar
- Flag
- Icon
- Illustration

### Navigation & Layout
- Accordion
- Dialog
- Drawer
- Dropdown
- Menu
- SideNav
- Tabs
- Stepper
- Timeline
- Divider
- Squircle
- Stack

### Other
- Search
- Tooltip
- Transaction
- File-Upload
- File-Output
- Segmented-Control
- Typography

---

## 📚 Documentation Format

Each component follows a **three-tier documentation model**:

1. **Overview** — Executive summary (2-3 min read)
2. **Guidelines** — Practical patterns (5-10 min read)
3. **Specs** — Technical reference (lookup only)

This structure helps:
- ✅ Designers understand when and how to use each component
- ✅ Developers find the exact tokens and props needed
- ✅ Teams align on accessibility and best practices
- ✅ New members onboard faster to the design system

---

## 🏆 Standards Applied

- **Accessibility**: WCAG 2.1 AA compliant
- **Mobile-First**: iOS & Android native patterns
- **Keyboard Navigation**: Full keyboard support
- **Screen Readers**: ARIA labels and semantic HTML
- **Color Blind Safe**: No color-only meaning
- **Touch Targets**: Minimum 44px (mobile)
- **Responsive**: Works across all breakpoints

---

## 🚀 Getting Started

1. **Find your component** in `Components/[ComponentName]/`
2. **Read Overview.md** to understand when to use it
3. **Check Guidelines.md** for best practices
4. **Reference Specs.md** for tokens and props
5. **Visit GitHub** for complete API and source code

---

## 📝 Last Updated

July 7, 2026

**Structure:**
- ✅ Overview files (Purpose, When to use, When not to use)
- ✅ Guidelines files (Patterns, Do/Don'ts, Imports)
- ✅ Specs files (Tokens, Props, Variants, Browser support)
- ✅ 48 components fully documented

---

For questions or contributions, visit the [GitHub repository](https://github.com/guillaumelopez78/Lumen-component-specs).
