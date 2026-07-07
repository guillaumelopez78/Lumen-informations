# Punctuation

## **Quick reference**

| **Mark** | **Rule** |
| --- | --- |
| **Full stop** | Complete sentences only: not headings, buttons, labels, placeholders |
| **Exclamation mark** | **Never use** |
| **Question mark** | **Never use in UI *(**see [Titles](../Titles%20314f148b3ab7807fa215de44d10c6f98.md))* |
| **Oxford comma** | Always use when itemising more than 3 articles |
| **Semicolon** | **Don't use:** *use shorter sentences or bullets* |
| **Quotation marks** | Straight double quotes **`" "`** in all languages |
| **Ellipsis** | In-progress states only: **`Processing payment...`** |
| **En dash –** | Ranges only, no spaces: **`10–20`   `9:00–17:00`** |

## **Full stops**

### **Use**

- Complete sentences in body copy, notifications, messages: **`Your payment has been processed.`**
- Error and warning messages: **`Payment failed. Please check your card details.`**
- Help text below fields, if it forms a complete sentence: **`Your IBAN will be validated automatically.`**
- Tooltips that are full sentences

### **Don't use**

- Headings and titles: **`Create new invoice.`**
- Buttons: **`Save changes.`**
- Form labels and table headers: **`E-mail address.`**
- Navigation items, single-word notifications, placeholder text
- Help text fragments: **`Maximum 50 characters.`**

## **Apostrophes & contractions**

- Contractions are fine in body copy and notifications: **`You'll receive a confirmation email.`**
- Use full forms in error messages and legal/critical contexts: **`Your payment cannot be processed.`**
- Possessives follow standard English: **`The company's invoice`**

## **Quotation marks**

- Always use straight double quotes **`" "`** in all languages, including French and German
- Use to reference UI labels or user input: **`Click "Save and continue"`**
- Place punctuation outside quotes unless it's part of the quoted text: **Click "Save", then review your invoice.**
- Never use for emphasis: use **bold** or *italics* instead.

## **Hyphens & en dashes**

| **Mark** | **Use for** | **Example** |
| --- | --- | --- |
| Hyphen **`-`** | Compound modifiers, prefixes | **`Two-factor authentication`**   **`Non-refundable`** |
| En dash **`–`** | Ranges — no spaces | **`10–20 transactions`**   **`9:00–17:00`**   **`15–20 Feb. 2026`** |

<aside>
⌨️

On macOS, en dash: **`Option** + **Shift** + **-**`

</aside>

## **Colons**

- Use to introduce lists, explanations, and key-value pairs: **`Payment status: pending`**
- Always lowercase after a colon, whether or not what follows is a complete sentence
- Exception: proper nouns retain their capital **`Provider: Stripe`**

## **Language-specific rules**

<aside>
🇫🇷

**French**

Add a non-breaking space *before* **`: ; ! ? " "`** 
Never before **`.`** or **`,`**

**`Statut : en attente`**
**`Êtes-vous sûr ?`**
**`Statut: en attente`**
**`Êtes-vous sûr?`**

</aside>

<aside>
🇩🇪

**German**

Add a comma before infinitive clauses.

**`Bitte klicken Sie hier, um fortzufahren.`**

</aside>

---

<aside>
💡

## Go further

### **Why no question marks in UI?**

Question marks in titles introduce doubt and slow decision-making. When a user clicks "Delete", the modal should confirm the action, not re-open the question. The same logic applies to all UI headings. See [Titles](../Titles%20314f148b3ab7807fa215de44d10c6f98.md)  and [Confirmation modals](../Confirmation%20modals%20311f148b3ab7804cb3f6c01197996de9.md).

### **Oxford comma in financial copy**

In transactional contexts, ambiguity is never acceptable. The Oxford comma prevents misreads in lists that carry legal or financial weight.

**`You can pay by card, bank transfer, or direct debit.`**
**`You can pay by card, bank transfer or direct debit.`**

### **Ellipsis**

Only for in-progress states. Never to trail off or imply uncertainty.

**`Processing payment...`**
**`We're not sure...`**

### **Accessibility**

Screen readers announce punctuation marks. Avoid stacking them **`!!`** or **`...`** in non-loading contexts, and never rely on punctuation alone to convey meaning.

</aside>