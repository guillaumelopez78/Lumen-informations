# Lumen Design System

**Professional component documentation system. Zero fluff.**

[![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen)]()
[![Components](https://img.shields.io/badge/Components-48-blue)]()
[![Coverage](https://img.shields.io/badge/Coverage-100%25-brightgreen)]()

---

## 🎯 Overview

Lumen is a minimalist, production-ready design system with 48 carefully crafted components for European fintech applications. Built for clarity, accessibility, and rapid development.

**Key Principles:**
- **Minimal Documentation** — Only what matters: "How to use", Guidelines (Do/Don't), Specs
- **Component-First** — 48 verified components across 9 categories
- **Product Focused** — Real product documentation for 4 key applications
- **Web + Mobile** — Complete coverage for React (web) and Native (mobile)

---

## 📁 Structure

```
lumen-component-specs/
├── README.md                          ← You are here
├── design-system/
│   └── Components/                    ← 48 component folders
│       ├── Accordion/
│       │   ├── Overview.md           (How to use)
│       │   ├── Guidelines.md         (Do/Don't table)
│       │   ├── Specs.md              (Design tokens & props)
│       │   └── Images/
│       ├── Button/
│       ├── TextField/
│       └── ... (45 more components)
└── product/                           ← 4 product documentation systems
    ├── Accounting/
    ├── Banking/
    ├── Cash-Pilot/
    └── Invoicing/
```

---

## 🎨 Component Categories

### Actions (3)
Button, Loader, Progress

### Feedback (4)
Alert, Banner, Callout, Toast

### Forms (11)
Autocomplete, Checkbox, DatePicker, File Upload, Multi-Select, Period Picker, Phone Input, Pin, Radio Button, Select, TextField, Text Area

### Layout (6)
Accordion, Divider, Squircle, Stack, Stepper, Switch

### Navigation (9)
Dialog, Drawer, Dropdown, Menu, Pagination, SideNav, Tabs, Segmented Control, Timeline

### Data Display (6)
Avatar, Badge, Card, Flag, Table, Tag

### Assets (3)
Icon, Illustration, Typography

### Other (3)
Search, Tooltip, Transaction

---

## 📊 Documentation Status

| Metric | Value | Status |
|--------|-------|--------|
| **Total Components** | 48 | ✅ Complete |
| **Documentation Coverage** | 100% | ✅ Complete |
| **Web (lumen-react)** | Stable v0.0.1 | ✅ Production |
| **Mobile (lumen-native)** | Stable v0.0.1 | ✅ Production |
| **Guidelines (Do/Don't)** | 48/48 | ✅ Complete |
| **Technical Specs** | 48/48 | ✅ Complete |
| **Product Systems** | 4 | ✅ Complete |

---

## 🚀 Quick Start

### Find a Component

Navigate to `design-system/Components/{ComponentName}/` and read in order:

1. **Overview.md** — When and how to use this component
2. **Guidelines.md** — Do's and Don'ts (best practices)
3. **Specs.md** — Technical details, props, design tokens

### Example: Button Component

```bash
design-system/Components/Button/
├── Overview.md      → When to use buttons, usage patterns
├── Guidelines.md    → Do: One accent button per screen max
├── Specs.md         → Props, variants, design tokens
└── Images/          → Screenshots and examples
```

### Explore Products

Each product has complete documentation with 6 sections:

```bash
product/Cash-Pilot/
├── 01_RESEARCH/           → User research, pain points, personas
├── 02_COMPETITIVE/        → Market analysis, competitor insights
├── 03_STRATEGY/           → Go-to-market, positioning, roadmap
├── 04_TECHNICAL/          → Architecture, technical decisions
├── 05_DESIGN_ASSETS/      → Figma files, design specifications
├── 06_DISCOVERY/          → Testing, validation, metrics
├── Overview.md            → Project summary
├── CHANGELOG.md           → Update history
└── Images/                → Screenshots and assets
```

---

## 💻 For Developers

### Web (React)

```tsx
import { Button } from '@shinetools/lumen-react';

<Button variant="filled" color="accent">
  Save Changes
</Button>
```

👉 **[Full Documentation](design-system/Components/Button/)**

### Mobile (Native)

```tsx
import { Button } from '@shinetools/lumen-native';

<Button variant="filled" color="accent">
  Save Changes
</Button>
```

👉 **[Full Documentation](design-system/Components/Button/)**

---

## 🎯 Products

### [Cash Pilot](product/Cash-Pilot/)
AI-powered cash flow forecasting for European SMBs
- **Status:** Shipped & Scaling (May 2026)
- **Markets:** France, Germany, Denmark, Netherlands
- **MVP:** 30-180 day cash forecasts from banking data

### [Invoicing](product/Invoicing/)
Simple, fast invoice creation and tracking

### [Banking](product/Banking/)
Banking operations and account management

### [Accounting](product/Accounting/)
Complete accounting and financial management

---

## 📖 Documentation Format

Each component follows a strict 3-file pattern:

### Overview.md
**Purpose:** Understand what this component does and when to use it.

Contains a "How to use" section explaining:
- When this component should be used
- When NOT to use it
- Usage patterns and context
- No code examples, no imports, no links

### Guidelines.md
**Purpose:** Best practices and anti-patterns.

Contains a Do/Don't comparison table:
- Actionable rules with real examples
- Text format only (no images)
- Rules ranked by importance

### Specs.md
**Purpose:** Technical reference for implementers.

Contains:
- Component props and variants
- Design tokens used
- Import paths
- Links to source code

---

## 🔗 Links

### Source Code
- 🌐 **Web (React):** https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react
- 📱 **Mobile (Native):** https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native

### GitHub Repository
- 📌 **This Repository:** https://github.com/guillaumelopez78/Lumendex

---

## 🛠️ Contributing

### Adding a New Component
1. Create `design-system/Components/{ComponentName}/`
2. Add **Overview.md** — How to use section
3. Add **Guidelines.md** — Do/Don't table
4. Add **Specs.md** — Props, tokens, API reference
5. Commit and push

### Updating Documentation
- Keep it minimal and focused
- Update CHANGELOG.md with date and summary
- Test on both web and mobile
- No breaking changes without notification

---

## 📊 Stats

| Metric | Value |
|--------|-------|
| Total Components | 48 |
| Documentation Files | 144+ (3 per component) |
| Product Systems | 4 |
| Product Sections | 6 per product |
| Design Tokens | 100+ |
| Accessibility | WCAG AA |
| Browser Support | Modern (Chrome, Safari, Firefox, Edge) |
| Mobile Support | iOS 13+, Android 8+ |

---

## 📞 Support

**Questions? Issues? Feedback?**
- 📧 Email: team@shine.co
- 💬 Slack: #design-system
- 🐛 Issues: GitHub Issues

---

**Last Updated:** July 7, 2026  
**Version:** 1.0.0  
**Status:** 🟢 Production Ready  
**Maintained By:** Design System Team
