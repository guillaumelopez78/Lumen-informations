# Date format

## **Quick reference**

| **Context** | **Format** | **Example** |
| --- | --- | --- |
| Standard | **`DD Mon YYYY`** | **`24 Feb 2026`** |
| Numeric | **`DD/MM/YYYY`** | **`24/02/2026`** |
| With time | **`DD/MM/YYYY, HH:MM`** | **`24/02/2026, 14:30`** |
| With day | **`Day, DD Mon YYYY`** | **`Mon, 24 Feb 2026`** |
| Date range | En dash, no spaces | **`28 Feb–5 Mar 2026`** |
| Technical / exports | **`YYYY/MM/DD`** | **`2026/02/24`** |
| Recent / upcoming (≤7 days) | Relative | **`2 days ago`**   **`In 3 days`** |

<aside>
👁️

When in doubt, use **`DD Mon YYYY`** to avoid DD/MM vs MM/DD ambiguity.

</aside>

## **Standard format**

- Day-first for all our markets: **`DD Mon YYYY`** or **`DD/MM/YYYY`**
- No ordinal indicators: **`24 Feb 2026`**   **`24th Feb 2026`**
- No full month names in constrained UI spaces
- Month abbreviations: no full stops in any language except French (see [below](Date%20format%20311f148b3ab780b48af0c9567e0f42fe.md))

## **Relative dates**

- Use relative terms within a 7-day window, past and future
- Beyond 7 days, switch to standard format

<aside>

**Past**

**`Today`**

**`Yesterday`**

**`2 days ago`**

**`5 days ago`**

</aside>

<aside>

**Future**

**`Tomorrow`**

**`In 3 days`**

**`Next Monday`**

</aside>

<aside>

**Beyond 7 days**

**`24 Feb 2026`**

**`24/02/2026`**

</aside>

## **Date ranges**

- Use en dash, no spaces **`Option + Hyphen`** on macOS
- Same month: **`15–20 Feb 2026`**
- Different months: **`28 Feb–5 Mar 2026`**
- Different years: **`20 Dec 2025–3 Jan 2026`**
- Avoid numeric for ranges: **`15/02/2026–20/02/2026`**

## Time format

- When displaying time alongside dates, use the 24-hour format for consistency across markets **`15 Feb 2026, 15:01`** **`20 Dec 2025, 09:23`** **`20 Dec 2025, 09:23 AM`**

## **Abbreviations by market**

#### Months

- Use **three-letter month abbreviations** as standard, with exceptions for months that have four letters or fewer in their full form
- No full stops except in French

| **Market** | **Jan** | **Feb** | **Mar** | **Apr** | **May** | **Jun** | **Jul** | **Aug** | **Sep** | **Oct** | **Nov** | **Dec** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 🇬🇧EN | Jan | Feb | Mar | Apr | May | Jun | Jul | Aug | Sep | Oct | Nov | Dec |
| 🇫🇷FR | jan. | fév. | mars | avr. | mai | juin | juil. | août | sep. | oct. | nov. | déc. |
| 🇩🇪DE | Jan | Feb | März | Apr | Mai | Jun | Jul | Aug | Sep | Okt | Nov | Dez |
| 🇳🇱NL | jan | feb | mrt | apr | mei | jun | jul | aug | sep | okt | nov | dec |
| 🇩🇰DK | jan | feb | mar | apr | maj | jun | jul | aug | sep | okt | nov | dec |

#### Days

| **Market** | **Mon** | **Tue** | **Wed** | **Thu** | **Fri** | **Sat** | **Sun** |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 🇬🇧EN | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
| 🇫🇷FR | lun. | mar. | mer. | jeu. | ven. | sam. | dim. |
| 🇩🇪DE | Mo | Di | Mi | Do | Fr | Sa | So |
| 🇳🇱NL | ma | di | wo | do | vr | za | zo |
| 🇩🇰DK | man | tir | ons | tor | fre | lør | søn |

<aside>
💡

EN/DE: capitalise months and days
FR/NL/DK: lowercase, except at the start of a sentence
→ See [Capitalisation rules](Capitalisation%202eff148b3ab780d0adfbd5e69d578bd9.md).

</aside>