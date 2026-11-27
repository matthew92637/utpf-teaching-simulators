# AI Gas Bottle — Instructions

File: `simulators/utpf-ai-gas-bottle-simulator.html`
(Open it in a browser. Nothing to install.)

## What this is

A small teaching market built from the video "Anthropic CEO lays it out: whether AI succeeds or fails, something big will happen."
Money (Q) rushes in first, the real output (V) arrives a year late, and expectations (T) run ahead of both.
Press a story button and watch the bottle break — or survive.

This is model-market behaviour, not a forecast of real stocks, and not investment advice.

## UTPF translation table

| In the video | Gas (UTPF) | Meaning here |
|---|---|---|
| Compute contracts: signed now, paid later | Q (money) | Compute contracts signed this year (units: $10 billion) |
| Real AI output, real revenue | V (volume) | What was actually made and sold this year |
| The price AI can charge | Π (pressure) | Shortage pushes the price up; surplus pushes it down |
| How hot expectations run | T (temperature) | Hotter expectations, hotter bottle; T = 1 + yearly growth rate |
| Household income, unpaid debts | The small bottle next door | AI takes jobs, household income falls, bad debts grow |
| Bank capital 26 | How thick the small bottle's wall is | Bad debts above 26 in one year, and the bank cannot hold |
| — | Z = ΠV / (QT) | How tight the bottle is: near 1 is healthy, below 0.5 is danger |

## Fixed assumptions (from the video's story, not measurements)

- 2026 is the first year; the company starts with cash 150.
- Household income starts at 100, household debt is 190; bank capital is 26.
- AI gets 10% more capable every year (up to 100%).
- New jobs: for every 10 jobs AI takes, about 6 become new jobs (0 in the unemployment-wave story).
- A prudent company watches Z and stops signing: it never signs new contracts that would push Z below 0.5.
  "Dario keeps buying" switches this brake off.

## How to play

1. Press a story button. The five years (2026–2030) run by themselves, stopping at the year something breaks, or at 2030.
2. "Run one year" steps one year at a time; "Run to 2030" runs the rest.
3. Move the sliders and checkboxes yourself: expectation heat, years to build a data centre, how capable AI really is, money one year late, the 3% tax, new goods, Dario keeps buying.
4. Watch three places: the Z line (below the red 0.5 line is danger), company cash (below zero is bankruptcy), bad debts (above 26 the bank cannot hold).

## Five worked examples

### Example 1: Amodei's ledger (company bankrupt, 2028)

Press "Amodei's ledger". Expectation heat 60%, data centre takes 1 year, customers' money one year late, Dario keeps buying.

| Year | Q contracts | V real output | Π | T | Z | Company cash |
|---|---|---|---|---|---|---|
| 2026 | 160 | 100 | 1.00 | 1.60 | 0.39 | 150 |
| 2027 | 256 | 160 | 0.88 | 1.60 | 0.34 | 78 |
| 2028 | 410 | 256 | 0.81 | 1.60 | 0.32 | −49 bankrupt |

In 2027 the contract money comes due, but customers' money is a year late: revenue is only 88 against 160 due.
In 2028 it is worse: 410 due against 129 of revenue, cash goes negative. The company is bankrupt — the bottle broke.
Exactly as the video says: in 2027 the money comes due, in 2028 the AI arrives, and the company is already gone.

### Example 2: Amodei's ledger, prudent (same numbers, company survives)

Press "Amodei's ledger, prudent". The numbers are identical to Example 1, except the company watches Z and stops signing.

| Year | Q contracts | V real output | Z | Company cash |
|---|---|---|---|---|
| 2026 | 125 | 100 | 0.50 | 150 |
| 2027 | 148 | 125 | 0.50 | 120 |
| 2028 | 190 | 148 | 0.50 | 123 |
| 2029 | 269 | 190 | 0.50 | 149 |
| 2030 | 431 | 269 | 0.50 | 224 |

The brake pins Z at 0.50 and the company survives all five years. Cash dips to 120 in 2027, then comes back to 224 by 2030.
The lesson: the same expectations, the same one-year delay — one brake is the difference between life and death.
Note: cash still fell in 2027, because the contracts signed in 2026 had to be paid in 2027. Stopping only helps if it starts a year early.

### Example 3: Bubble bursts (AI is not that capable, bankrupt 2028)

Press "Bubble bursts". Expectation heat 80%, AI only 60% as capable, customers' money one year late, Dario keeps buying.

| Year | Q contracts | V real output | Z | Company cash |
|---|---|---|---|---|
| 2026 | 180 | 60 | 0.20 | 115 |
| 2027 | 324 | 126 | 0.20 | 30 |
| 2028 | 583 | 259 | 0.21 | −143 bankrupt |

Z stays around 0.20 from start to finish: the most money rushing in, the least real output. Cash goes to −143 in 2028.
This is the dot-com story Burry tells: the product is not that capable, but the money rushes in anyway.

### Example 4: Unemployment wave (company fine, bank dead, 2028)

Press "Unemployment wave". AI succeeds at once (no waiting), and there are no new jobs.

| Year | Company cash | Household income | Bad debts this year |
|---|---|---|---|
| 2026 | 150 | 100 | 0 |
| 2027 | 150 | 91 | 17.1 |
| 2028 | 150 | 77 | 44.5 bank cannot hold |

Nothing happens to the company: cash stays at 150, Z stays at 0.63.
But household income falls 100 → 91 → 77, and bad debts of 44.5 pass bank capital of 26.
The lesson: the bottle that breaks is not always the AI company — it can be the bank next door. The trouble travels from the unemployed person to the bank that lent to them.

### Example 5: Third outcome (new things grow, households end better off)

Press "Third outcome". It starts like Amodei's ledger, but with the 3% tax, new cures and new goods growing from 2028, and expectations cooling from 2029.

| Year | Z | Company cash | Household income | Bad debts |
|---|---|---|---|---|
| 2026 | 0.50 | 150 | 103 | 0 |
| 2027 | 0.50 | 120 | 104 | 0 |
| 2028 | 0.67 | 194 | 110 | 0 |
| 2029 | 0.71 | 375 | 118 | 0 |
| 2030 | 0.50 | 468 | 120 | 0 |

Nobody breaks. Z climbs back from 0.50 to 0.71, and household income rises from 100 to 120 — better off, not worse.
Now press "Third outcome, no tax" and compare: the company does exactly as well, but household income falls all the way to 81,
and in 2030 bad debts of 35.6 break the bank. The tax is the whole difference.

## Honest limits

- This is a teaching model, not a forecast. The story numbers (cash 150, debt 190, bank capital 26, new goods +100 a year) are assumptions, not measurements. Different assumptions give different results.
- Z is computed from the translation, not measured in a real market. The operational definition of T in UTPF is still being pinned down.
- Nothing here is investment advice. Do not buy or sell anything from these numbers.
