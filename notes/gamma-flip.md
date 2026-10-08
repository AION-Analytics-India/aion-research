# The Gamma Flip: When Dealers Stop Damping and Start Amplifying

Published October 8, 2026 · AION Analytics (India) · Lokesh Gupta

Canonical version: <https://aionanalytics.in/research/notes/gamma-flip>

DOI: [10.5281/zenodo.23227411](https://doi.org/10.5281/zenodo.23227411)

---
The gamma flip is the price at which the net gamma of option dealers changes sign. On one side their hedging leans against every move. On the other it adds to every move. Crossing it changes how the market behaves.

The note on Max Pain describes a market that is pinned. The note on gamma squeeze mechanics describes one that accelerates. They are not two different markets. They are two states of the same one, and the gamma flip is the level that separates them.

## Two states

Gamma measures how fast the delta of an option changes as price moves. A dealer who hedges with futures is in one of two states, depending on the sign of the gamma across the whole book.

- **Long gamma.** The dealer holds more bought options than sold ones. When price rises, the dealer sells futures to stay hedged. When price falls, the dealer buys. The hedging leans against every move, and volatility is damped. This is the pin.
- **Short gamma.** The dealer has sold more options than bought. When price rises, the dealer must buy futures. When price falls, the dealer must sell. The hedging adds to every move, and volatility is amplified. This is the squeeze.

## The flip

A dealer's book is spread across many strikes, so its net gamma is not one fixed number. It changes as spot moves from strike to strike. The gamma flip is the price at which the total changes sign.

In the case drawn below, dealers are long gamma under the flip and short gamma over it. Below the flip they dampen. Above it they amplify.

<div class="diagram">

![Two panels on one price axis with a horizontal line marking the gamma flip. Left: below the line price moves in small fading swings with arrows pointing inward; above the line the swings grow with arrows pointing outward. Right: a curve of dealer gamma exposure, positive below the flip and negative above it, crossing zero at the flip.](images/gamma_flip_regimes.svg)

Figure 1. Price behaviour on each side of the gamma flip, and dealer gamma exposure crossing zero at that level. Schematic, not market data.

</div>

## Which side amplifies is not fixed

The figure shows one arrangement: dealers have sold Calls at the strikes above and hold bought options below. That is the book behind an upside squeeze, and it is the case this set of notes has followed.

The arrangement can be the other way round. Where investors mostly sell Calls for income and buy Puts for protection, the dealers who take the other side are long gamma above the flip and short gamma below it. In that market it is falls that accelerate and rallies that grind. The flip is defined by the change of sign. Which side amplifies depends on what the dealers have actually bought and sold.

## Why it matters

The flip level does not appear on the option chain. It has to be estimated from open interest, implied volatility, and an assumption about which side of each contract the dealers hold.

When price crosses it, the market changes regime. A move that would have been absorbed an hour earlier is now a move that feeds itself. Nothing in the news needs to change for this to happen. Only the sign of the hedging has changed.

## A practical reading

With the arrangement in the figure, spot below the estimated flip and rising toward it tends to make slow, grinding progress, because each rise is met by hedging supply. Once spot is above the flip, the same rise is met by hedging demand and the move speeds up. The logic runs in reverse on the way back down: a fall through the flip takes price from the amplifying side to the damping side, and the move loses force.

This is also why the three checks in the Max Pain note sit beside a caution. A pin that looks stable can be close to a level where the hedging behind it turns over.

## What this note does not claim

The flip is an estimate, not an observation. Exchange data does not show who holds which side of an option, so every published flip level rests on an assumption about dealer positioning. If the assumption is wrong, the level is wrong, and the two sides may be the wrong way round as well.

Dealer books also change during the day. A level computed from the previous evening's open interest can be stale by mid-morning. No hit rate is claimed here for moves that follow a crossing, and this note does not offer a way to compute the level.

<div class="tags">

<span class="tag">Gamma flip</span><span class="tag">Dealer gamma</span><span class="tag">Long gamma</span><span class="tag">Short gamma</span><span class="tag">Hedging flows</span><span class="tag">Volatility regimes</span>

</div>
