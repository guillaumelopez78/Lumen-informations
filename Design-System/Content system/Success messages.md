# Success messages

## How to write a success message:

<aside>
💡

Success messages should always explain what has just been accomplished immediately when it’s achieved, not a few moments later. 

It can also reassure the users on the action they just did. 

If a next step is awaited, communicate it to the user.

</aside>

<aside>
⚠️

Do not congratulate as it could be seen as to infantilise.

</aside>

- Start with either the subject that has just been completed or “Your” if the user is initiating the successful action: **`Your bank account has been connected.`** , **`Your invoice has been sent.`** , **`Congratulations! Your bank account is now connected.`** , **`Operation done.`**

#### IF success message is a snackbar

- Be as short and concise
- Use the present perfect passive structure `Your` + `X` + `has been` + `action verb`
→ **`Your Stripe has been disconnected.`**

#### IF success message is a full screen (empty state)

- **Title** has to explain what has been accomplished and if there is a next step
- **Copy** adds necessary context if needed. It’s an opportunity to add personality to surprise or engage the user
- **CTAs** are optional but we encourage you to put at least an action to help the user

<aside>

**`Your new card is on its way`**
`It will be delivered between 3 to 5 business days. You can create a virtual card in the meantime if needed.`

<aside>

Go to my dashboard

</aside>

<aside>

Create a virtual card

</aside>

</aside>

#### IF success message is a modal

- **Title** has to be task-specific. Thus, they use an action verb and no ponctuation
- **Copy** adds necessary context if needed. Those modals are an opportunity to add personality to surprise or engage the user. Don’t ask unnecessary questions
- **CTAs** are responses to the title and clarify the action they will do

<aside>

**`Confirm your address`**
`Your new card is on its way. It will be send to this address:
5 Rue de la Paix, 75002 Paris`

<aside>

Edit address

</aside>

<aside>

Send to this address

</aside>

</aside>

<aside>
💡

**Should I use a modal, a snackbar or an empty state?**

Modal initiates a conversation where an action is needed.
Snackbar gives an immediate feedback for the user’s actions.
A modal should never be used if an action is not needed from the user.

Empty states is pretty much like a modal, but without anything to display behind it (because of a redirection or because it’s the end of a funnel, for example) and no mandatory action to do.

</aside>