# UTPF Teaching Simulators

Free, browser-based classroom simulators that show how a market works like a gas — and how four great schools of economics look when you test them side by side.

**Play now — no install, no account, no cost.** Download this repository, double-click any simulator file, and it opens in your browser.

## The simulators

| Simulator | File | What it does |
|---|---|---|
| Farmers Market | [utpf-farmers-market-gas-simulator.html](simulators/utpf-farmers-market-gas-simulator.html) | The market as a gas: shoppers on one side, farmers on the other, a sliding counter between them. Where the counter rests is the price. |
| Farmers Market — Four Schools wind tunnel | [utpf-farmers-market-four-schools.html](simulators/utpf-farmers-market-four-schools.html) | The same market run four ways — Smith, Keynes, Friedman, Marx — for 30 seconds each, scored side by side. |
| Farmers Market — Traditional Chinese, simple language | [utpf-farmers-market-gas-simulator-kids-zh.html](simulators/utpf-farmers-market-gas-simulator-kids-zh.html) | The farmers-market simulator with Traditional Chinese labels in simple words. |
| Short-Term Forecast | [utpf-gas-piston-forecast-simulator.html](simulators/utpf-gas-piston-forecast-simulator.html) | Shows an 80% cone around the coming week, so students learn what a forecast can and cannot say. |
| Short-Term Forecast — Traditional Chinese | [utpf-gas-piston-forecast-simulator-tc.html](simulators/utpf-gas-piston-forecast-simulator-tc.html) | The forecast simulator in Traditional Chinese. |
| IS-LM Gas Lab | [utpf-is-lm-gas-simulator.html](simulators/utpf-is-lm-gas-simulator.html) | The textbook IS-LM model in a gas picture: output Y is volume, money M is gas, interest r is temperature, and the liquidity trap is absolute zero. |
| Phillips Curve Gas Lab | [utpf-phillips-curve-simulator.html](simulators/utpf-phillips-curve-simulator.html) | The textbook expectations-augmented Phillips curve in a gas picture: unemployment is idle gas, expected inflation is temperature, and the long-run curve stands straight at the natural rate. |

## The big idea

A market behaves like a gas. Each person at the market is like a gas molecule, bouncing around. Pressure is measured from the dots hitting the walls and the counter — nothing is assumed. The counter slides until the two pressures balance, and where it rests is the price. The market obeys an equation of state, Π·V = Z·Q·T, where Z is the market's health number: Z = 1 is an ideal gas, above 1 the crowd packs in, below 1 the market freezes and herds.

## The four schools wind tunnel

One market, four regimes, one yardstick. Each run lasts 30 seconds.

| Regime | Setting | What happens |
|---|---|---|
| Smith — laissez-faire | 80 shoppers, 80 farmers, nobody touches the market | The market settles by itself in about 5–7 seconds. |
| Keynes — stimulus | 130 eager shoppers, plus a stimulus dose (+$150 or +$600) | The highest price and the most trades — and the market never settles. The size of the dose matters. |
| Friedman — fixed money | Same as Smith, but the wallet grows by $4.50 every second | The market stays calm and settles in about 7–8 seconds. |
| Marx — concentration | The same goods, held by only 12 big sellers | Trades slow down and the market never settles. |

Press **▶ Run all four (2 min)** to run them all and compare the score table.

## For teachers

- A 30-minute classroom activity. Students run the simulators, write down the numbers, and argue about what they mean.
- No account, no installation, no grade impact.
- [`teaching/simulator-tester-brief-en.md`](teaching/simulator-tester-brief-en.md) — a one-page brief for testers, with five feedback questions.
- [`teaching/simulator-test-procedure-en-zh.md`](teaching/simulator-test-procedure-en-zh.md) — a step-by-step test procedure in English and Traditional Chinese.
- [`manuals/utpf-four-schools-user-manual.pdf`](manuals/utpf-four-schools-user-manual.pdf) — a full user manual with worked examples, in English first, then Traditional Chinese in simple language.
- [`manuals/utpf-gas-piston-forecast-manual-en.pdf`](manuals/utpf-gas-piston-forecast-manual-en.pdf) and [`utpf-gas-piston-forecast-manual-zh.pdf`](manuals/utpf-gas-piston-forecast-manual-zh.pdf) — the forecast simulator's manual.
- [`manuals/is-lm-gas-simulator-instructions-en.md`](manuals/is-lm-gas-simulator-instructions-en.md) and [`is-lm-gas-simulator-instructions-tc.md`](manuals/is-lm-gas-simulator-instructions-tc.md) — the IS-LM Gas Lab's instructions, in English and in Traditional Chinese simple language, with five worked examples and the liquidity-trap test.
- [`manuals/phillips-curve-simulator-instructions-en.md`](manuals/phillips-curve-simulator-instructions-en.md) and [`phillips-curve-simulator-instructions-tc.md`](manuals/phillips-curve-simulator-instructions-tc.md) — the Phillips Curve Gas Lab's instructions, in English and in Traditional Chinese simple language, with five worked examples and the expectations chain from the short run to the long run.

## Manuals and measurement

- `manuals/` — the user manuals above.
- [`measurement/utpf-four-schools-measurement-sheet-tc.md`](measurement/utpf-four-schools-measurement-sheet-tc.md) — the five-part yardstick: four schools × five dimensions, each cell saying what to measure, how to compute it, and what counts as passing (Traditional Chinese, simple language).
- [`measurement/utpf-four-schools-test-conditions-tc.md`](measurement/utpf-four-schools-test-conditions-tc.md) and [`utpf-four-schools-test-conditions-en.md`](measurement/utpf-four-schools-test-conditions-en.md) — the detailed test conditions and results, in Traditional Chinese and English.

## Honest limits — please read this

- These are **model-market** numbers, not real-market forecasts, and **not investment advice**. Do not buy or sell anything because of a number in these simulators.
- The entropy number S is a price-distribution proxy, not the full trajectory entropy described in the paper. The market's "temperature" T still has no settled operational definition.
- Each run differs a little, because the market has random noise in it. Run two or three times before drawing a conclusion.
- The paper's yardstick has five parts. Four passed; the fourth — predicting real markets — is only half-passed, because no real-market data has been run through the test yet.

## What is NOT here

There is no trading terminal here, no trading formulas, and no stock advice. The research-grade tools are held back until a non-disclosure agreement or a second patent filing. Only the teaching simulators are shared.

## Further reading

- The validation plan for the gas-chamber simulator, published on Zenodo: https://doi.org/10.5281/zenodo.23649620
- The working paper behind the four-schools wind tunnel, "Measuring How UTPF Assists the Major Schools of Economic Thought" (November 15, 2026, discussion draft, not peer-reviewed) — Zenodo link to be added when the draft is deposited.

## License

Code is released under the MIT License (see `LICENSE`). Documents are released under CC BY 4.0. Confirmed by the author, 2026-11-23.

## Contact

Matthew Yen, Emeritus Professor, California State University, Fresno — matthewy@mail.fresnostate.edu

Shared freely for classrooms, in the spirit of Micah 6:8 — act justly, love mercy, walk humbly with God.
