# IS-LM Gas Lab — Instructions

> File: `utpf-is-lm-gas-simulator.html` (open it in a browser and play)
> Written in plain language. All numbers come from inside the simulator, not from a real stock market. Do not use them to buy or sell anything.

## 1. What is IS-LM?

IS-LM is a famous diagram drawn by Hicks in 1937 to explain Keynes. It asks one question: **at what interest rate, and at what level of income, are two markets happy at the same time?**

There are two lines in the picture:

- **IS (the goods market):** investment equals saving. When the interest rate is low, borrowing is cheap, firms invest, people spend, and income is high. When the rate is high, investment falls and income falls. So the IS line slopes down: lower rate, higher income.
- **LM (the money market):** the money people want to hold equals the money the central bank has printed. When income is high, people need more cash; with money in short supply, the rate must rise. So the LM line slopes up: higher income, higher rate.

**Where the two lines cross is the answer.** That point's interest rate and income are where both markets are satisfied, and the economy rests there.

## 2. How does it relate to UTPF?

Your UTPF treats the market as a gas: pressure Π, volume V, gas amount Q, temperature T, with ΠV = Z·Q·T. IS-LM translates into that picture whole:

| IS-LM | Gas (UTPF) | Plain meaning |
|---|---|---|
| Output Y (income) | Volume V | How big the market container is |
| Price level P (fixed at 1.00, short run) | Pressure Π | Stays at 1.00 — prices do not move in this short-run picture |
| Money supply M | Gas amount Q | How many money particles are in the vessel |
| Interest rate r | Temperature T | How hot the market runs (your book's mapping: r is temperature) |
| Animal spirits (confidence) | Heater setting | Hopeful moods raise investment and push IS right |
| — | Z = ΠV / (QT) | Computed from the mapping; near 1 is the calm baseline |

**Why is the translation reasonable?** The Keynesian story is already "two markets pushing each other" — the goods market and the money market. The gas story is also "particles and a piston pushing each other." The IS-LM equilibrium point is where the piston stops moving. Government spending is a push on the piston from outside; the central bank printing money is adding gas to the vessel.

**The trap is absolute zero.** When the interest rate r falls to 0, temperature T is 0, the denominator of Z is zero, and Z cannot be computed. That is not a bug in the program — it is the model speaking: at absolute zero the gas law breaks down. At that point only government spending can move the piston; adding gas does nothing.

## 3. How to play

### Sliders (drag one and the curves and the piston follow at once)

- **Government spending G** (0–100, starts at 40): how much the government spends on roads, payments, and so on.
- **Money supply M** (50–200, starts at 100): how much money the central bank has printed.
- **Market confidence** (0.5–1.5, starts at 1.00): whether people feel hopeful or afraid about the future. High confidence raises investment.
- **Investment sensitivity to r (d)** (5–20, starts at 10): how much investment moves when the rate moves a little.
- **Money-demand sensitivity to r (h)** (5–50, starts at 10): how much cash people want to hold when the rate moves a little. In trap mode h becomes 1000.

Fixed in this lab: price level P = 1.00, taxes = 20, marginal propensity to consume = 0.8, autonomous consumption = 20, autonomous investment = 30, money-demand sensitivity to income k = 0.5. The interest rate cannot go below 0%.

### Five story buttons (press one and watch the dot travel)

1. **Normal day**: back to the starting settings.
2. **Recession — confidence falls**: people get afraid and investment shrinks.
3. **Government stimulus**: the government spends 20 more.
4. **Central bank prints money**: money goes from 100 to 150.
5. **Liquidity trap**: confidence 0.5, government spending 20, h = 1000, the rate stuck at 0%.

### Two trap-test buttons

- **Trap test: print +$50**: M goes up by 50.
- **Trap test: spend +$20**: G goes up by 20.

Use these two inside the trap: printing should do almost nothing, spending should do a lot.

### Two pictures

- **IS-LM diagram**: the blue line is IS, the orange line is LM, the red dot is where both markets clear at once. The dot is labelled with Y* and r*. Press a story button and the dot travels.
- **Gas piston**: the piston's position is output V; the dots are money particles Q; the thermometer on the right is the interest rate T; pressure Π stays at 1.00 because the price level is fixed.

### Score table

Every story or test button press adds one row: story name, Y before, Y after, r before, r after, Z after. **Clear table** empties it.

## 4. Five worked examples, one by one

Each example starts from "Normal day": Y* = 248.6, r* = 2.43%, Z = 1.02.

### Example 1: Normal day

- Settings: G = 40, M = 100, confidence = 1.00.
- Result: Y* = 248.6, r* = 2.43%, Z = 1.02.
- Reading: Z near 1 is the calm baseline. The piston sits in the middle, the thermometer reads 2.43%.

### Example 2: Recession, confidence falls

- Press **Recession**: confidence falls from 1.00 to 0.60.
- Result: Y* falls from 248.6 to 231.4, r* falls from 2.43% to 1.57%, Z becomes 1.47.
- Reading: people are afraid, investment shrinks, IS shifts left, income and the rate fall together. Z above 1 is like the gas turning stiff and hard to push.

### Example 3: Government stimulus

- Press **Government stimulus**: G goes from 40 to 60.
- Result: Y* rises from 248.6 to 277.1, r* rises from 2.43% to 3.86%, Z becomes 0.72.
- Reading: government spending shifts IS right and income rises — but everyone competing to borrow pushes the rate up too. Z below 1 is like the gas turning soft and easy to push.

### Example 4: Central bank prints money

- Press **Central bank prints money**: M goes from 100 to 150.
- Result: Y* rises from 248.6 to 320.0, r* falls from 2.43% to 1.00%, Z becomes 2.13.
- Reading: more money shifts LM right, the rate falls, income rises. Z rises above 1 because the temperature fell by more than the gas grew.

### Example 5: Liquidity trap

- Press **Liquidity trap**: confidence 0.50, G = 20, h = 1000.
- Result: Y* falls from 248.6 to 195.0, r* falls from 2.43% to 0%, Z shows "—".
- Reading: the rate is stuck at 0%, the temperature is at absolute zero, and Z cannot be computed. The piston sits far to the left and the thermometer is at the bottom.

## 5. The trap test: printing does nothing, spending works

First press **Liquidity trap** (Y* = 195.0, r* = 0%), then run the two tests:

| Test | How | Result |
|---|---|---|
| Print money | Press **print +$50**, M goes from 100 to 150 | Y* stays 195.0, r* stays 0%. Printing does nothing at all. |
| Spend money | Press **spend +$20**, G goes from 20 to 40 | Y* jumps from 195.0 to 295.0, r* stays 0%. Spending works. |

That is the most important Keynesian lesson: **when the rate is at zero, the central bank printing money cannot move the economy — only government spending can.** Your four-schools wind tunnel tells the same story in the Keynes regime: the small +$150 stimulus does not move it, the large +$600 stimulus does.

## 6. How to read Z

- **Z ≈ 1**: the calm baseline; money circulates at its usual speed.
- **Z > 1**: the gas is stiffer, the market is harder to push (1.47 in the recession, 2.13 after printing money).
- **Z < 1**: the gas is softer, the market is easier to push (0.72 after government spending).
- **Z shows "—"**: temperature T is too close to 0 for Z to mean anything. The rate is at zero — that is the trap.

Said honestly: the way to read Z is an aid to imagination, not a law. Z is computed from the mapping, not measured from a real market.

## 7. Honest limits

1. This is a teaching model, not a forecast. Short run only, the price level is assumed fixed, the economy is closed, and the lines are drawn straight on purpose.
2. The gas numbers are IS-LM numbers translated, not measured. Z is computed from the mapping; it is a way to see the model, not a law of nature.
3. The interest rate never goes below 0% — that is a floor built into the model. In the real world rates can go slightly negative, but this little lab does not play that game.
4. Nothing here can be used to buy or sell stocks. It is only a tool for understanding economics.

## 8. Questions to ask next

- If the price level P could move too (not fixed at 1.00), what would happen to the piston and the pressure gauge?
- If the country traded with the rest of the world (add exports and imports), how would the IS line change?
- In your UTPF, the working definition of temperature T is still not pinned down. This lab defines T as the interest rate r. Do you think that definition is good? Is there a better one?
- In the four-schools wind tunnel, the Keynes stimulus doses (+$150, +$600) and the G + 20 here — do the effects look alike?

---

*Verification note: the simulator's mathematics was checked by computer. The five story numbers (248.6 / 231.4 / 277.1 / 320.0 / 195.0) and the trap test (printing does nothing, spending jumps to 295.0) all match. The original farmers-market simulator was not touched.*
