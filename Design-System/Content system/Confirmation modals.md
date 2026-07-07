# Confirmation modals

<aside>

Confirmation modals appear when users are about to take a significant or irreversible action. They serve as a final checkpoint, helping users avoid mistakes whilst not creating unnecessary friction.

**See also:**
[IF success message is a modal](Success%20messages%20313f148b3ab780eeb0fff967e2235cf7.md) 
[IF warning display is modal](Warning%20messages%20313f148b3ab7804ca469caacd09b848e.md) 
[IF error display is modal or fullpage](Error%20messages%202bef148b3ab78020bc1bf78228783dbf.md) 

</aside>

## How to write a confirmation modal:

#### Title

- State the action as an affirmative — never a question
- Use sentence case
- Be specific when it helps: **`Delete draft invoice`** **`Delete`**
- **2–4 words: `Delete quote`** , **`Remove client`** , **`Export transaction data` `Are you sure you want to cancel this payment?`**

<aside>
💡

**Why affirmations over questions?**

- Questions introduce doubt and slow decision-making: "Do you want to delete this invoice?" makes the user reconsider whether deletion is the right choice
- Affirmations state what's happening clearly: "Delete invoice" confirms the action without second-guessing
- Users have already initiated the action (clicked "Delete") – the modal confirms intent, not introduces new questions
</aside>

#### Body

- Never repeat the title
- Add what the title doesn't say: consequence, scope, or reassurance
    - Explains consequences **`This action cannot be undone`**
    - Highlights what will be lost **`All associated payment data will be permanently removed`**
    - Clarifies scope **`This will remove access for 3 team members`**
    - Provides reassurance **`Your data will be exported as a CSV file and sent to you directly`**
    - Sets expectations **`The customer will be notified by email`**

#### CTA

- Primary: mirrors the title in intent
- Secondary: always **`Return`** or **`Dismiss`** — never **`Cancel`**
- Avoid **`Yes, delete`** — the "Yes" adds nothing

#### Example

<aside>

**Delete QUOTE-0001**
Deleting a quote removes it permanently.

<aside>

Return

</aside>

<aside>

Delete permanently

</aside>

</aside>

<aside>

**Delete this quote?**
If you delete this quote, you’re going to loose it forever.

<aside>

Cancel

</aside>

<aside>

Confirm delete

</aside>

</aside>