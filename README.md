# Lumen Brain

Single source of truth for Shine's design system and product knowledge.

---

## 📁 Structure

```
Lumen-Brain/
├── README.md
├── Design-System/
│   ├── Composants/            ← 48 component folders (Overview, Guidelines, Specs)
│   └── Content system/        ← UX writing rules, tone of voice, copy templates
└── Product/                   ← Product knowledge for 4 Shine products
    ├── Accounting/
    ├── Banking/
    ├── Cash-Pilot/
    └── Invoicing/
```

---

## 🎨 Design-System

### Composants

48 components, each documented with the same three files:

- **Overview.md** — "How to use": when this component applies, when it doesn't
- **Guidelines.md** — Do/Don't table of best practices
- **Specs.md** — Props, variants, design tokens, source code links

**Categories:**

| Category | Components |
|---|---|
| Actions | Button, Loader, Progress |
| Feedback | Alert, Banner, Callout, Toast |
| Forms | Autocomplete, Checkbox, DatePicker, File Upload, Multi-Select, Period Picker, Phone Input, Pin, Radio Button, Select, TextField, Text Area |
| Layout | Accordion, Divider, Squircle, Stack, Stepper, Switch |
| Navigation | Dialog, Drawer, Dropdown, Menu, Pagination, SideNav, Tabs, Segmented Control, Timeline |
| Data Display | Avatar, Badge, Card, Flag, Table, Tag |
| Assets | Icon, Illustration, Typography |
| Other | Search, Tooltip, Transaction |

### Content system

UX writing rules and copy references, shared across products:

- **Formatting** — Numbers, dates, currencies, punctuation, capitalisation
- **Language** — Anglicisms, British vs. American English, tone, localisation, language-sensitive components per market (DK, NL, FR, DE)
- **Tone & Voice** — Action-oriented writing, help & support saved responses
- **Accessibility** — Inclusive language
- **Template library** — Ready-to-use copy templates (buttons, empty states, errors, modals) with EN/FR pairs
- **Features names** — Canonical feature names and descriptions per domain (Banking, Accounting, Invoicing)
- Page-level copy guides: CTA buttons, modals, notifications, error/success/warning messages, empty states, onboarding, inputs, links, titles

---

## 🎯 Product

Product knowledge for Shine's 4 core products. Each product folder follows the same 6-section structure:

```
Product/{ProductName}/
├── 01_RESEARCH/          → User research, interviews, personas, pain points
├── 02_COMPETITIVE/       → Competitor profiles, market landscape
├── 03_STRATEGY/          → Positioning, go-to-market, market sizing
├── 04_TECHNICAL/         → Architecture notes, technical decisions
├── 05_DESIGN_ASSETS/     → Figma references, design specifications
├── 06_DISCOVERY/         → Usability testing, validation, metrics
├── ARCHIVE/              → Superseded documents kept for history
├── Overview.md           → Project summary
├── CHANGELOG.md          → Documentation update log
└── sources.md            → Source tracking (Notion, etc.)
```

- **[Cash Pilot](Product/Cash-Pilot/)** — AI-powered cash flow forecasting for European SMBs. Shipped & scaling (May 2026), live in France, Germany, Denmark, Netherlands. Most complete section: 10 user interviews, 27 competitor profiles, market sizing, Maze test results.
- **[Invoicing](Product/Invoicing/)** — Invoice creation and tracking.
- **[Banking](Product/Banking/)** — Banking operations and account management.
- **[Accounting](Product/Accounting/)** — Accounting and financial management.

---

## 🔗 Source Code

- 🌐 **Web (lumen-react):** https://github.com/shinetools/shine-ui/tree/main/libs/lumen-react
- 📱 **Mobile (lumen-native):** https://github.com/shinetools/shine-ui/tree/main/libs/lumen-native

---

**Last Updated:** July 7, 2026
