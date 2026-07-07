# Numbers

## How to write numbers:

<aside>
👁️

For date formatting, see [Date format](Date%20format%20311f148b3ab780b48af0c9567e0f42fe.md). For currency symbols, see [Currencies](Currencies%20311f148b3ab78062b501db07943e5e16.md).

</aside>

#### **Quick reference**

| **Type** | **Format** | **Example** |
| --- | --- | --- |
| Monetary amounts | Numeral + currency code | `1,250.50 EUR` |
| Percentages (all markets) | Numeral + % no space | `15%` `2.5%` |
| Percentages (FR) | Numeral + non-breaking space + % | `15 %` |
| Ranges | En dash, no spaces | `10–20 items` `5–7 business days` |
| Large numbers (UI) | Full numerals | `1,250,000 EUR` |
| Large numbers (dashboards) | Abbreviated + unit | `1.25M EUR` `3.4K transactions` |
| Negative numbers | Minus sign before number | `−50.00 EUR` |

#### **Numerals vs words**

- Use numerals for amounts, quantities, percentages, dates, and technical values **`You have 3 pending transactions and 12 completed ones.`**
- Write out in words only when starting a sentence or restructure to avoid it **`Three payment methods are available.`**
- Never mix formats in the same context **`You have three pending transactions and 12 completed ones.`**

#### **Thousand separators & decimals**

- Always 2 decimal places for currencies **`50.00 EUR`**
- For percentages, use whole numbers for general references (**`15%`**) and one decimal when precision matters (**`2.5%`**)

<aside>
🇬🇧

**UK & US**

Thousands: comma **`,`**

Decimals: full stop **`.`**

**`1,250.50`**

</aside>

<aside>
🇪🇺

**EU markets**

Thousands: **`space`** (FR, DK) or full stop **`.`** (DE, NL)

Decimals: comma **`,`**

**`1 250,50`**  /  **`1.250,50`**

</aside>

<aside>
🇫🇷

**Three non-breaking space rules:**

To do non-breaking space on Mac: **`Option + Space`**

**Thousand separator:**

- Always a non-breaking space **`1 250,50`**

**Percentage:**

- Non-breaking space between number and % **`15 %`**

**Currency:**

- Non-breaking space before the currency code
- Currency goes after the amount **`1 250,50 EUR`**
</aside>

#### **Ranges**

- En dash, no spaces **`Option + Hyphen`** on macOS.
- In running text, prefer **`to`** or **`between…and`** for readability **`Processing takes 1 to 3 business days.`**
- En dash is fine in tables, labels, and constrained UI spaces **`10–20 transactions`**

#### **Ordinal numbers**

- Use ordinal words for step sequencing and informal references: **`first transaction`**, **`one-off payment`**
- Use ordinal numerals in lists and UI: **`1st`**, **`2nd`**, **`3rd`**.
- Never use ordinals in dates, see [Date format](Date%20format%20311f148b3ab780b48af0c9567e0f42fe.md): **`24 Feb 2026`**   **`24th Feb 2026`**

**Ordinal format by market**

| **Market** | **1st** | **2nd** | **3rd** | **4th+** | **Note** |
| --- | --- | --- | --- | --- | --- |
| 🇬🇧 EN | 1st | 2nd | 3rd | 4th | st / nd / rd / th |
| 🇫🇷 FR | 1er / 1re | 2e | 3e | 4e | 1er masc., 1re fem. |
| 🇩🇪 DE | 1. | 2. | 3. | 4. | Full stop after numeral |
| 🇳🇱 NL | 1e | 2e | 3e | 4e | Lowercase e |
| 🇩🇰 DK | 1. | 2. | 3. | 4. | Full stop after numeral |

## Go further

<aside>

<aside>

#### **Large numbers**

</aside>

**When to abbreviate**

Use full numerals in all financial UI copy. Abbreviated forms (K, M, B) are acceptable only in data visualisations and dashboards where space is limited, always followed by the unit:

- **`1,250,000 EUR`** in transaction details
- **`1.25M GBP`** or **`450K transactions`** in a dashboard widget
- Always uppercase **`K`**, **`M`**, **`B`**

<aside>

#### **Special formats**

</aside>

**Phone numbers**

Format with country code and spaces to group digits.

- 🇬🇧 **`+44 20 7123 4567`**
- 🇫🇷 **`+33 1 23 45 67 89`**
- 🇩🇪 / 🇳🇱 / 🇩🇰 Use spaces to group digits after country code
- International fallback: group digits with spaces for readability

**Account & reference numbers**

Group every 4 digits for readability: **`1234 5678 9012 3456`   `1234567890123456`**

**International transfers**

For currencies without subdivisions (e.g. JPY, KRW in international wire transfers), use zero decimal places: **`10000 JPY`**. See [Currencies](Currencies%20311f148b3ab78062b501db07943e5e16.md) for full guidance.

<aside>

#### **Accessibility**

</aside>

**Numbers and assistive technologies**

- Always use numerals for data that screen readers announce precisely: amounts, quantities, dates.
- No Roman numerals (**`I, II, III`**)
- Always provide context for standalone numbers: **`3 items`** is clearer than just **`3`**.
</aside>