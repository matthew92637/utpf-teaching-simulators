# Phillips Curve Gas Lab — Instructions

> File: `utpf-phillips-curve-simulator.html` (open it in a browser and play)
> Written in simple language. All numbers are the simulator's numbers, not the real economy. Nothing here is for buying or selling stocks.

## 1. What is the Phillips curve?

In 1958, an economist named Phillips drew a picture. Unemployment is across the bottom, inflation is up the side, and the line slopes down, like a slide:

- **Low unemployment, high inflation.** Plenty of jobs, bosses compete for workers and raise wages; making things costs more, so prices rise.
- **High unemployment, low inflation.** Many people out of work, nobody dares ask for a raise, prices stay still.

**But expectations push the whole curve up.** Given time, everyone starts to expect prices to rise, workers ask for raises first, bosses raise prices first. Result: unemployment does not fall, inflation rises anyway, and the whole curve moves up a notch. Keep doing that and unemployment returns to a place called the "natural rate", where the curve stands straight up.

**Once, the curve seemed broken.** In the 1970s the oil price suddenly jumped, things got expensive, and jobs disappeared too. High unemployment AND high inflation, both bad friends together. People call it "stagflation".

## 2. How does it connect to UTPF?

Your UTPF sees the market as a gas: pressure Π, volume V, gas amount Q, temperature T, with ΠV = Z·Q·T. The Phillips curve translates into that picture completely:

| Phillips curve | Gas | In plain words |
|---|---|---|
| Unemployment rate u | Idle work (Q − V) / Q | The share of the gas not doing work |
| Inflation rate π | Pressure Π = 1 + π/100 | How hard prices push on the vessel wall |
| Employment V = 100 − u | Volume V | How much of the gas is working |
| Labour force (100 people) | Gas amount Q = 100 | All the workers |
| Expected inflation π^e | Temperature T = 1 + π^e/100 | How hot expectations run in everyone's head |
| Supply shock v (oil) | Wind from outside | A gust blows the whole curve up |
| — | Z = ΠV / (QT) | Computed from the mapping; near 1 is the calm baseline |

**Why is this translation reasonable?** Unemployment is the idle part of the gas; expectations are the temperature — the hotter everyone's head, the hotter the whole pot, the higher the pressure. An oil shock is like a hot wind blowing in from outside: the whole pot heats up, but the piston does no extra work.

## 3. How to play

### Sliders (drag them, the picture and the piston follow at once)

- **Demand heat** (0–100, starts at 50): how hot the economy runs. Drag it up, more jobs, less unemployment; drag it down, fewer jobs, more unemployment.
- **Expected inflation π^e** (0–8%, starts at 2.0%): how much people in their heads think prices will rise. This is the temperature.
- **Natural rate of unemployment u_n** (3–6%, starts at 4.5%): where unemployment rests when the economy is calm.

Fixed in this lab: slope a = 0.6, labour force Q = 100, formula π = π^e − 0.6·(u − u_n) + supply shock. Unemployment stays between 1% and 12% on this chart.

### Four story buttons (press one, watch the dot travel)

1. **Normal day**: back to the starting settings.
2. **Hot economy**: demand goes from 50 to 75, more jobs.
3. **Recession**: demand goes from 50 to 30, fewer jobs.
4. **Stagflation — oil shock**: demand 30, supply shock +3%.

### Four action buttons

- **Central bank raises rates**: demand −10, the economy cools.
- **Stimulus: heat demand +10**: demand +10, the economy heats up.
- **Oil shock +3**: supply shock +3%, demand −10.
- **Expectations catch up**: what people expect becomes equal to today's inflation.

### Two pictures

- **Phillips curve diagram**: the blue line is the short-run curve (drawn from today's expectations), the grey dashed line is the long-run curve (standing straight at the natural rate), the red dot is where the economy is now. Press a story button and the dot walks.
- **Gas piston**: the piston's position is employment V; the little dots are the labour force Q; the thermometer on the right is expectations T; pressure Π = 1 + π/100.

### Score table

Every time you press a story or action button, the table gains a row: story name, u before, u after, π before, π after, Z after. Press **Clear table** to empty it.

## 4. Five worked examples, one by one

Every example starts from "Normal day": u = 4.5%, π = 2.0%, Z = 0.95.

### Example 1: Normal day

- Settings: demand = 50, expected inflation = 2.0%, supply shock = 0.
- Result: u = 4.5%, π = 2.0%, Z = 0.95.
- How to read it: unemployment sits exactly at the natural rate, inflation exactly equals what people expected. The piston rests in the middle, the thermometer reads 2.0%.

### Example 2: Hot economy

- Press **Hot economy**: demand goes from 50 to 75.
- Result: u falls from 4.5% to 2.0%, π rises from 2.0% to 3.5%, Z becomes 0.99.
- How to read it: more jobs, the dot slides up the short-run curve. Less unemployment, more inflation.

### Example 3: Recession

- Press **Recession**: demand goes from 50 to 30.
- Result: u rises from 4.5% to 6.5%, π falls from 2.0% to 0.8%, Z becomes 0.92.
- How to read it: fewer jobs, the dot slides down the short-run curve. More unemployment, less inflation.

### Example 4: Stagflation

- Press **Stagflation**: demand 30, supply shock +3%.
- Result: u rises from 4.5% to 6.5%, π rises from 2.0% to 3.8%, Z becomes 0.95.
- How to read it: unemployment high AND inflation high. The dot did not walk along the curve — the whole curve moved up by itself. The oil wind heated the whole pot.

### Example 5: Oil shock (starting from normal)

- Press **Oil shock +3**: supply shock becomes +3%, demand goes from 50 to 40.
- Result: u rises from 4.5% to 5.5%, π rises from 2.0% to 4.4%, Z becomes 0.97.
- How to read it: oil gets expensive, things get expensive, jobs get scarce. Both sides get worse — that is why central banks fear oil prices most.

## 5. The expectations chain: from the short run to the long run

This is the most important exercise. Press three steps in order:

| Step | What to do | u | π | What happens |
|---|---|---|---|---|
| 1. Hot economy | Press **Hot economy** | 2.0% | 3.5% | The dot slides up the short-run curve |
| 2. Expectations catch up | Press **Expectations catch up** | 2.0% | 5.0% | The whole curve shifts up, inflation rises again |
| 3. Cool down | Drag the demand slider back to 50 | 4.5% | 3.5% | Unemployment returns to the natural rate, but inflation stays high |

That is why the long-run curve is vertical: **if you keep pushing unemployment below the natural rate, inflation keeps running up; in the end unemployment returns to 4.5% anyway, only with higher inflation.** In the short run you can trade, in the long run you cannot.

## 6. How to read Z

- **Z ≈ 0.95**: the calm baseline (normal day and the long-run point are both 0.95).
- **Z a little higher (0.99)**: hot economy, the gas is fuller.
- **Z a little lower (0.92)**: recession, the gas is emptier.
- **Honestly**: in this little lab Z moves very little, because inflation Π and expectations T usually move together and cancel each other out. Z is nearly the same as the employment rate (how many people have jobs). That does not mean Z is useless — it means Π and T are tied too tightly together in this experiment.

Reading Z is a way to imagine, not a law. Z is computed from the mapping, not measured from a real market.

## 7. Honest limits

1. This is a teaching model, not a forecast. A textbook simplification; real inflation also moves with productivity, world oil prices, and slow policy, none of which are in this lab.
2. The gas numbers are the Phillips numbers translated, not measured. Z is computed from the mapping, not a law of nature.
3. The slope a = 0.6 and the natural rate 4.5% are fixed assumptions; in the real world both numbers move and drift over time.
4. Nothing here is for buying or selling stocks. This is only a tool for understanding economics.
5. The operational definition of temperature T is still unpinned: this lab sets T = 1 + expected inflation, as a proposal, not a conclusion.

## 8. Questions to ask next

- If the natural rate u_n drifts over time (say people learn new skills), how does the long-run curve move?
- If the price level Π also moves inside the IS-LM piston, can the two labs be joined into one?
- For the 2021–22 inflation, your Z dashboard said no overheat; what would the Phillips curve say? Walking along the curve, or the curve shifting?
- In your UTPF, the operational definition of T is still unpinned. This lab sets T to expected inflation — is that a good definition? Is there a better one?
- What does an oil shock look like in your farmers' market? Like a sudden wind blowing into the market?

---

*Verification record: the simulator's mathematics was checked by computer. The four stories (normal 4.5% / 2.0%, hot 2.0% / 3.5%, recession 6.5% / 0.8%, stagflation 6.5% / 3.8%), the oil shock (5.5% / 4.4%), and the expectations chain (3.5% → 5.0% → back to 4.5% / 3.5%) all match. The original farmers-market simulator was not touched.*
