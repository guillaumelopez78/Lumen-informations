# Currencies

## How to write currencies:

- Format: **`amount`** + **`currency code`**
- Use a non-breaking space between amount and code: **`Option + Space`** on macOS
- Never abbreviate or use symbols: **`EUR`**   **`€`**
- Always include the code even for zero amounts: **`0.00 EUR`**

**⚠️ Never assume a default currency, even in localised contexts.**

## **Specific cases**

#### **Ranges**

- En dash, no spaces, code after the second amount: **`50–100 GBP`**

#### **Multiple currencies**

- Always make both codes visible when comparing amounts: **`1,250.00 EUR / 1,065.00 GBP`**

<aside>
🇫🇷

#### French non-breaking space

- All spaces are non-breaking: thousand separator, before %, and before the currency code **`1 250,00 EUR`**
- Non-breaking space before **`EUR`**
- Non-breaking space as thousand separator
</aside>

## Go further

<aside>
💡

### **Why codes over symbols?**

Three-letter codes are more reliably pronounced by screen readers than symbols. **`€`** may be read as "euro sign" or skipped entirely depending on the assistive technology, while **`EUR`** is unambiguous. Codes also work better with translation tools and are internationally consistent.

Also, some countries doesn’t use symbols but letters (DKK / Kr.) which cause interface issues in our product such as readability for the user, especially in tables.

### **Transition note**

Existing products may still use currency symbols or mixed formats. These are acceptable during the transition to a unified product. The target standard is the three-letter code format documented here.

</aside>