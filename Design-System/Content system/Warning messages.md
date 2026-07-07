# Warning messages

## How to write a warning message:

<aside>

**What differentiate a warning from an error message?**

A warning message alerts users of a condition that might cause a problem in the future.
An error message alerts of an issue that has already occurred.

|  | ⚠️ **Warning** | 🚨 **Error** |
| --- | --- | --- |
| *When* | Issue hasn't happened yet | Issue has already occurred |
| *Tone* | Anticipatory, calm | Factual, solution-focused |
| *Example* | **`You have 10 days before account closure.`** | **`Your payment could not be processed.`** |
</aside>

#### IF warning display is **inline**

- One sentence
- Follow the structure: **`condition`** + **`deadline / consequence`**
- No exclamation marks

→ **`Maintenance is planned this afternoon. Disconnections can occur.` `Warning! The platform will be unavailable for some time`**

#### IF warning display is modal

**Title**

- State what's at risk
- Use sentence case
- No alarming words **`Warning`** **`Attention!`**
- **2–5 words: `Payment details needed`**

**Body**

- Follow this structure: **`What’s happening`** + **`what to do` + `deadline`**
- Keep in within 1–3 sentences
- Don't repeat the title

→ **`To keep your account running, add payment details by March 3, 2026.`**

**CTA**

- One or two buttons — fix the issue, or check the status: **`Add payment details`**, **`Try again`**, **`Check Stripe's status`**

#### Examples

<aside>
✅

**Stripe may be temporally unavailable**

We’re running into some connection difficulties with Stripe at the moment.

<aside>

Try again

</aside>

<aside>

Check Stripe’s status

</aside>

</aside>

<aside>
✅

**Payment details needed**

To keep your account running, add payment details by March 3, 2026.

<aside>

Add payment details

</aside>

</aside>

<aside>
🚫

**Having trouble connecting?**

Something went wrong and you can’t connect.

<aside>

OK

</aside>

</aside>

<aside>
🚫

**We're going to close your account**

You need to pay before the end the period.

<aside>

Learn more

</aside>

</aside>

## Patterns to follow/avoid

| **Pattern** | **Instead** |
| --- | --- |
| Alarm words | `Warning!` → let context carry the urgency |
| Question titles | `Having trouble?` → `Stripe may be temporarily unavailable` |
| Vague consequences | `unavailable sometimes` → `Disconnections can occur this afternoon` |
| Weak CTAs | `Learn more` → `Add payment details` or `Check Stripe's status` |
| Threats | `We're going to close your account` → `You have 10 days before account closure` |