# Gamma Squeeze Mechanics: Why Dealers Accelerate Their Own Pain

Published October 8, 2026 · AION Analytics (India) · Lokesh Gupta

Canonical version: <https://aionanalytics.in/research/notes/gamma-squeeze>

DOI: [10.5281/zenodo.23226817](https://doi.org/10.5281/zenodo.23226817)

---
A gamma squeeze is a feedback loop. Dealers who have sold Calls must buy the underlying as it rises, their buying lifts the price, and the higher price forces them to buy more. Nobody plans it. It comes out of the hedging rules.

The phrase gamma squeeze became famous through single stocks, but the mechanism is general and it appears in index options too. It is worth understanding step by step, because the people doing the buying in a squeeze are usually not bullish. They are hedging.

## The mechanism, one step at a time

1. **Dealers sell Call options.** The buyers are often retail traders. The dealers are now short those Calls.
2. **The underlying rises toward the strike.** The short Call position starts to lose money.
3. **The dealers buy the underlying to stay delta-neutral.** This is the key point. As price rises, the delta of the Call rises as well, so the dealers need to hold more of the underlying against it, not less.
4. **That buying pushes the price higher.**
5. **The higher price raises delta again.** More buying is needed, which lifts the price again.

That is the loop. Each pass through it makes the next pass larger.

<div class="diagram">

![A loop of four steps. Dealers have sold Calls. Price rises toward the strike. Dealers buy the underlying to hedge. Price rises further. In the centre, a computer server running on a treadmill, labelled dealer hedging engine. A side note lists the three ways the squeeze breaks.](images/gamma_squeeze_feedback_loop.svg)

Figure 1. The hedging loop behind a gamma squeeze, and what ends it. Schematic, not market data.

</div>

## Why the hedge keeps growing

Delta is the share of a move in the underlying that shows up in the option price. Gamma is how fast delta itself changes. A dealer who is short Calls is short gamma, which means every rise in price leaves the existing hedge too small.

A small example, with invented numbers, shows the size of the effect. Suppose a desk is short 10,000 Call contracts and the delta of each is 0.30. To be hedged it holds the equivalent of 3,000 contracts of the underlying. Price moves up toward the strike and delta becomes 0.45. The hedge now has to be 4,500. The desk must buy 1,500 more, at the higher price. If that buying moves price again and delta reaches 0.60, it must buy another 1,500.

Gamma is largest when the option is close to the money and close to expiry. That is why squeezes tend to happen near a heavily traded strike in the final days of a contract, and rarely far from one.

## How it ends

The loop accelerates until one of three things happens.

- **The options expire.** The open interest disappears and so does the need to hedge it.
- **The dealers run out of capital to hedge.** Positions are cut or closed, sometimes at a heavy loss.
- **The buying exhausts itself.** Once the Calls are deep in the money, delta is close to 1 and has little room left to rise. The forced buying fades.

## An index squeeze is not a single-stock squeeze

A gamma squeeze in Nifty does not look like the one in GameStop. An index has far deeper liquidity, and no one can corner it. What shows up in an index is a sudden, violent move through a strike that traps two groups at once: Call buyers who chase the breakout after most of the move is done, and Put writers who are stopped out on the way.

The dealers are not trying to squeeze anyone. They are hedging by rule. The squeeze is what those rules produce when many desks follow them at the same time, in the same direction.

## What makes a squeeze more likely

- **Open interest concentrated at one strike close to spot.** The hedging need is then bunched at one price.
- **Low float or thin liquidity in the underlying.** In a single stock this is the free float. In an index it is the depth of the futures market at that moment.
- **A sudden catalyst that carries price through the strike.** Without a first push the loop does not start.
- **Large short gamma exposure among dealers.** This is often reported as GEX, for gamma exposure.

## What this note does not claim

Exchange data shows how many contracts are open at each strike. It does not show who is long, who is short, or who is hedging. Every published GEX number therefore rests on an assumption about which side the dealers hold. When that assumption is wrong, the sign of the estimate is wrong with it.

The steps above also describe the upside case only. The same loop runs in reverse through Put strikes, where dealers who are short Puts must sell as price falls. This note describes a mechanism. It does not offer a way to predict when a squeeze will begin.

<div class="tags">

<span class="tag">Gamma squeeze</span><span class="tag">Delta hedging</span><span class="tag">Short gamma</span><span class="tag">Open interest</span><span class="tag">Options expiry</span><span class="tag">Feedback loops</span>

</div>
