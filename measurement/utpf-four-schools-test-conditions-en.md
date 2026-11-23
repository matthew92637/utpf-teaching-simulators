# Four-Schools Wind-Tunnel Test: Test Conditions, Steps, Parameters, and Conclusions

A version in simple words. Source: the paper "Measuring How UTPF Assists the Major Schools of Economic Thought" (November 15, 2026, discussion draft); the test site: the farmers-market simulator, four-schools mode `utpf-farmers-market-four-schools.html`; the measurement sheet: `utpf-four-schools-measurement-sheet-tc.md`.

In one sentence: the same market, four ways to play, one ruler. Run it, then compare.

## Part 1: Test conditions (the same for all four ways)

Just like a race needs everyone to agree on how long the track is and how to decide the winner, our track is set like this:

**The same market**
- What is sold: apples, customary price $3.00 a crate
- The farmers bring 180 crates in total
- The shoppers bring $900 in total
- The piston (the market counter) starts in the middle, so the price starts at $3.00

**The same way to measure**
- Price P: where the piston rests, that is the price
- Pressure gap ΔΠ: the buyers' push minus the sellers' push
- Z: how healthy the market is. 1 is the standard.
- Free energy F: how much pressure is stored in the market
- Money M: the shoppers' wallets plus the farmers' cash box
- Number of trades: how many crates were sold
- Entropy S: how jumpy the price is (calculated from how the price is spread out; it is an approximation)

**The same time**
- Each way runs for 30 seconds
- A number is written down every 0.5 seconds, 60 numbers in total
- When you press a play button, the market resets and starts over

**When do we say "it has settled"?**
- The pressure gap |ΔΠ| is less than 0.05, and the piston speed is less than 8, for 3 seconds in a row. Only then do we say it has settled.
- The first 5 seconds do not count, because the pressure has not been measured yet.

**When do we say "it is pinned"?**
- The piston is pushed all the way to the end and cannot move, like a pipe that is blocked.

**Fair rules**
- We only change the settings of each way to play. We do not change the physics. The gas rules (ZNORM 626, how the piston moves, the customary-price spring) are the same for all four ways.
- There is a little randomness in the market, like the weather being a little different every day. So the numbers from one run will be a little different each time. Run each way two or three times and look at the general picture. Do not trust only one run.

## Part 2: The four schools, one by one

### Smith: the government does nothing. Let the market run by itself.

**What is this school asking?**
Is the invisible hand real? After the market is scared, does it come back to calm by itself?

**Parameters (press the "Smith" button and the simulator sets them for you)**
| Setting | Number | What it means |
|---|---|---|
| Buyer temperature TD | 0.95 | Shoppers feel normal |
| Buyer count QD | 80 | 80 shoppers |
| Seller temperature TS | 0.95 | Farmers feel normal |
| Seller count QS | 80 | 80 farmers |
| Money growth | 0 | The government prints no money |
| Stimulus money | 0 | The government spends no money |

**Steps**
1. Press the "Smith" button. The market resets and starts running.
2. Watch where the price starts, and how long it takes to come back near $3.00.
3. Press the "shove the piston" button to give the market a scare. Measure how many seconds the price takes to come back to $3.00. That number of seconds is called the return time, τ.
4. Shove it again. If the two shoves are closer together than τ, see whether the price keeps failing to come back.
5. After 30 seconds, press "Stop & score" and look at that row in the score table.

**Numbers to watch**
- The return time τ, in seconds
- When it settles, how far the price is from $3.00
- If two scares come too close together, does the price keep failing to come back?

**Conclusion**
The market really does come back by itself. In the test run, the price came back to about $3.06 and settled in about 6.7 seconds, very close to the customary price. The invisible hand really moves in this little market. But be careful: if the scares come one after another, faster than 6.7 seconds, the market may keep failing to come back. That prediction needs to be tested a few more times before it counts.

### Keynes: the government spends money and gives demand a push

**What is this school asking?**
The market is stuck in a bad place and cannot climb out. If the government spends money to push it, does it work? How much money is enough?

**Parameters (press the "Keynes" button and the simulator sets them for you)**
| Setting | Number | What it means |
|---|---|---|
| Buyer temperature TD | 1.60 | Shoppers are very eager |
| Buyer count QD | 130 | 130 shoppers, more than before |
| Seller temperature TS | 0.95 | Farmers feel normal |
| Seller count QS | 80 | 80 farmers |
| Money growth | 0 | This is spending money, not printing money |
| Small stimulus dose | +$150 | Like the year 2009 |
| Large stimulus dose | +$600 | Like the year 2020 |

**Steps**
1. Press the "Keynes" button. The market resets and starts running.
2. First do not press any stimulus money. Watch whether the market gets stuck.
3. Press "Small stimulus +$150." Watch whether the price moves.
4. Then press "Large stimulus +$600." Watch whether the price jumps.
5. Add the dose little by little. Write down the smallest dose that brings the price back near $3.00. That is the least money needed.
6. After 30 seconds, press "Stop & score" and look at that row in the score table.

**Numbers to watch**
- Did the small dose move it? Did the large dose move it?
- What is the smallest stimulus that brings the price back?
- How high did the price go? Did the number of trades go up or down?

**Conclusion**
Giving demand a push really pushes the price up. In the test run, the average price was $3.60, 20% above the customary price, and there were 72 trades, more than usual. But the price never settled down in 30 seconds. The line between "the small dose does not move it" and "the large dose moves it" is the height of the wall you have to climb out of the hole. In 2009 the stimulus was not enough, and in 2020 it was enough. You can understand that comparison by pressing the buttons in the simulator yourself.

### Friedman: money grows at a fixed speed, no matter what the market does

**What is this school asking?**
The money formula MV = PQ is like the formula for an ideal gas. Where does it work, and where does it stop working?

**Parameters (press the "Friedman" button and the simulator sets them for you)**
| Setting | Number | What it means |
|---|---|---|
| Buyer temperature TD | 0.95 | Shoppers feel normal |
| Buyer count QD | 80 | 80 shoppers |
| Seller temperature TS | 0.95 | Farmers feel normal |
| Seller count QS | 80 | 80 farmers |
| Money growth | +$4.5 every second | 0.5% of $900 per second, fixed and never changing |
| Stimulus money | 0 | No spending, only printing money |

**Steps**
1. Press the "Friedman" button. The market resets and starts running.
2. Watch whether Z stays close to 1. Z close to 1 means it acts like an ideal gas.
3. Write down the average of |Z−1|. That is the error of the formula.
4. Change the money growth speed by hand, faster and slower, and watch whether the error grows with it.
5. After 30 seconds, press "Stop & score" and look at that row in the score table.

**Numbers to watch**
- The average of |Z−1|. Less than 0.15 means the formula still works.
- How many seconds until the price comes back to $3.00
- When the money growth becomes messy, does the error grow with it?

**Conclusion**
When money grows at a fixed speed, the market is very calm. In the test run, the price came back to about $3.06, settled in about 7.6 seconds, and the average error of Z was only 0.12. The ideal-gas formula mostly works in this little market. But the error is not zero. The messier the money grows, the bigger the error becomes. When the error goes above 0.15, that is when the formula stops working.

### Marx: the sellers become a few big players

**What is this school asking?**
When things pile up more and more in a few hands, does the market become tight? Does a crisis come suddenly when the pressure reaches one point?

**Parameters (press the "Marx" button and the simulator sets them for you)**
| Setting | Number | What it means |
|---|---|---|
| Buyer temperature TD | 0.95 | Shoppers feel normal |
| Buyer count QD | 80 | 80 shoppers |
| Seller temperature TS | 1.60 | The big sellers push very hard |
| Seller count QS | 12 | Only 12 big sellers are left |
| Total stock | 180 crates, unchanged | Each big seller holds about 15 crates |
| Money growth | 0 | The government prints no money |
| Stimulus money | 0 | The government spends no money |

**Steps**
1. Press the "Marx" button. The market resets and starts running.
2. Watch whether the price is higher than usual, and whether there are fewer trades.
3. Watch whether the free energy F keeps climbing, and whether the piston gets pinned.
4. Write down the F at the moment the piston gets pinned. That is the critical value.
5. Add sellers one by one (raise QS up from 12). See how many sellers it takes before the piston comes loose.
6. After 30 seconds, press "Stop & score" and look at that row in the score table.

**Numbers to watch**
- How much higher the price is, and how many fewer trades there are
- Does F keep climbing?
- Does the piston get pinned? If it does, what is F at that moment?
- How many sellers do you have to add before the piston comes loose?

**Conclusion**
When there are fewer sellers, the market really becomes tight. In the test run, the average price was $3.28, higher than usual, there were only 26 trades, much fewer than usual, and the market never settled in 30 seconds. But this time the piston did not get pinned, so the prediction "a crisis will surely come" did not happen in this test run. How many sellers you have to add to loosen it still needs to be tested. The stored pressure F and its critical value are the most important new numbers for this school.

## Part 3: All four side by side (the test-run score table)

Below are the results from a headless test run in the computer on November 16, 2026, each way run for 30 seconds. The numbers will be a little different each time you run it. That is normal.

| Way | Average price | Price jumpiness | Farthest from customary | Seconds to settle | Pinned? | Formula error \|Z−1\| | Pressure F | Trades | Messiness S |
|---|---|---|---|---|---|---|---|---|---|
| Smith | $3.06 | $0.13 | 15.4% | 6.7 s | No | 0.128 | 0.00 | 46 | 0.69 |
| Keynes | $3.60 | $0.19 | 24.7% | Never settled | No | 0.124 | −0.23 | 72 | 0.49 |
| Friedman | $3.06 | $0.17 | 19.1% | 7.6 s | No | 0.121 | 0.00 | 46 | 0.87 |
| Marx | $3.28 | $0.14 | 13.7% | Never settled | No | 0.106 | −0.07 | 26 | 0.19 |

How to read this table:
- The average prices closest to $3.00 are Smith and Friedman. Keynes is the highest, Marx is second highest.
- The fastest to settle is Smith (6.7 seconds), then Friedman (7.6 seconds). Keynes and Marx never settled in 30 seconds.
- The most trades are in Keynes (72). The fewest are in Marx (26).
- The formula errors are all about the same (0.106 to 0.128), all inside 0.15.

## Part 4: Final conclusions (the five marks, how many passed?)

**Mark 1: Is the translation right? Passed.**
All four schools' ideas fit into the simulator: the piston, the pressure, the temperature, and the free energy all match.

**Mark 2: Are there new numbers we can calculate? Passed.**
We now have new numbers that the simulator can calculate: the return time, the height of the wall, the error of the formula, and the stored pressure.

**Mark 3: Are there new predictions? Passed, and written down.**
Each school now has one prediction that can be checked: Smith says if the scares come too close together, the market will not come back. Marx says when the pressure crosses the line, the piston will get pinned. Keynes says the small dose will not move it but the large dose will. Friedman says when the money grows messily, the error will grow. These predictions still need to be tested a few more times.

**Mark 4: Are the predictions more accurate? Only half passed.**
Inside the model, we can use one run's result to guess the next run's result. That works. But we have not yet checked it with real market data, because we do not have that data yet.

**Mark 5: Can the medicine dose be calculated? Passed.**
For Keynes the dose can be measured (the smallest stimulus that works). For Friedman the dose is the money growth speed itself. For Marx the dose is how many sellers to add. For Smith the dose is zero (do nothing).

**One last sentence**
UTPF's help is this: it turns "it is probably like this" into states we can measure, doses we can calculate, and predictions we can check. This wind tunnel can already run, and the four ways really are different. But remember: these numbers are from a game market, not the real stock market. They cannot be used to buy stocks.

*Note: the test-run numbers will be a little different each time, because there is randomness in the market. Entropy S is an approximation from how the price is spread out, not the trajectory entropy the paper talks about. How to measure temperature T is not fully settled yet. The original paper is a discussion draft. It has not been peer-reviewed.*
