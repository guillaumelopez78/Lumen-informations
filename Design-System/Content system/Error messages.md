# Error messages

## How to write an error message:

<aside>
💡

The subject of the message should remain **the object of the error** — it should never be us, nor the user.

- Blaming ourselves too easily for the error may undermine trust and make the product seem unreliable
- Blaming the user should also be avoided, as it creates guilt and negatively impacts their experience
</aside>

- Start with the subject of the action **`The IBAN number` `Your invoice contains errors`**
- Then, tell what’s wrong **`doesn't match the account holder's name`**
- If possible, offer the solution **`Please review the highlighted fields` `Check the information in the incorrect fields`**
- Or reassure **`No funds have been taken from your account`**

#### IF error display is **inline** or **field error**

- Help the user fix an issue *immediately* within a form or action field: **`Your first name is required here.`** , **`Please enter a valid IBAN.` ,** **`Only supported formats are: .JPG, .PNG and .PDF.`**
- Keep it under 10 words.

#### IF error display is modal or fullpage

- Aim for 2–3 short sentences max.
- Follow this pattern: **What happened** → **What to do next** → (Optional) **Why it happened**
→ **`The transaction couldn’t be completed. No funds have been taken from your account.`
→`This account doesn’t currently have enough funds to process the transfer. To proceed, please top up your account first.`** 
→ **`Some features are temporarily unavailable due to a technical issue. You can continue using the rest of the app normally. Updates will be posted here as soon as possible.`**
→ **`We couldn’t load this page. Please refresh your browser or try again in a few minutes. If the problem persists, contact support for help.`**

<aside>

## Formatting

**Capitalisation**

Always use sentence case for error messages, not title case. Capitalise only product-specific terms (e.g., IBAN, CSV, PDF).

**`Please enter a valid IBAN.`** **`Please Enter a Valid Iban.`**

**Punctuation**

End all error messages with a full stop, even short ones.
No exclamation marks — they can sound alarming or overly emotional.

**`Enter a valid email address.`** **`Enter a valid email address`**

**Links**

Hyperlink actionable items: **`increase your limits here`** , **`contact support`**
Use descriptive link text — never **`click here`** or **`learn more`** alone.

**`Contact support for help`** **`Click here`**

**Accessibility**

- Don't rely on colour alone to communicate errors. Always include text.
- Ensure error messages have sufficient colour contrast (WCAG AA minimum: 4.5:1).
- Use `aria-live` regions for dynamic error messages so screen readers announce them.
</aside>