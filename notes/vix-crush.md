# The VIX Crush: Why Your Option Loses Value Even When You Are Right

Published October 8, 2026 · AION Analytics (India) · Lokesh Gupta

Canonical version: <https://aionanalytics.in/research/notes/vix-crush>

DOI: [10.5281/zenodo.23226819](https://doi.org/10.5281/zenodo.23226819)

---
An option buyer pays for direction and for fear. At the open the uncertainty is resolved, implied volatility falls, and the fear part of the premium drains out. The option can lose value on a day when the direction was correct.

You buy a Put because you expect the market to fall. The market falls. The Put should be worth more. By 9:20 AM it is down 40%. Nothing went wrong with the view. Something else in the price changed.

Traders call this the VIX crush, or the IV crush. Strictly, what falls is the implied volatility of the option that was bought. India VIX is the index that summarises implied volatility across Nifty options, so the two usually move together.

## What you pay for when you buy an option

Implied volatility, or IV, is the market's estimate of how much the underlying will move in the future. It is read backwards from option prices. When uncertainty is high, people pay more for options and IV is high.

An option buyer is therefore paying for two things at once.

- **Direction.** The sensitivity of the premium to a move in the underlying is called delta.
- **Fear.** The sensitivity of the premium to a change in IV is called vega.

At 9:15 AM the fear part of the premium is at its largest. A few minutes later most of it can be gone.

## The mechanics

1. **Overnight, uncertainty builds.** Global markets move, news arrives, and nobody can trade the index. IV rises.
2. **At the opening bell, the uncertainty is resolved.** The gap happens. The news is in the price.
3. **IV falls.** The part of the premium that vega was holding up drains away.
4. **The option loses value.** The fear premium has gone. The direction was not wrong.

<div class="diagram">

![Chart of the change in an option's premium from 9:15 AM to 10:30 AM. Delta profit rises. Vega loss falls sharply in the first minutes. Net premium rises briefly and then falls below the entry premium. A shaded band marks the profit window from 9:15 to 9:20 AM.](images/vix_crush_premium_decay.svg)

Figure 1. Delta profit, vega loss and the net premium after the open. Schematic, not market data.

</div>

## A small example

The numbers here are invented to show the arithmetic. A Put is bought at the open for a premium of 100. It has a delta of 0.5 in absolute terms and a vega of 4, meaning the premium changes by 4 for every one-point change in IV.

| What changed | Size of the change | Effect on the premium |
|---|---|---|
| Index falls, as expected | 40 points | +20 |
| IV falls after the open | 10 points | -40 |
| Net |  | -20 |

The premium is now 80. The view on direction earned 20. The fall in IV cost 40. The trader was right about the market and still lost a fifth of the premium.

## The window is short

For a directional view on an index expressed through bought options at the open, the window in which the trade can pay is not the whole day. It is roughly the first 5 to 15 minutes. In that time the move in the underlying can outrun the fall in IV. After that, falling IV and time decay, which is called theta, take premium away faster than delta can add it.

The figure shows the narrow version of this, a window that closes by 9:20 AM. How long the window stays open on a given morning depends on how much IV has to fall and how far the index keeps moving.

## What to look at

The reading that matters is the at-the-money IV on the option chain.

- **Above about 20:** the fear premium is rich and has a long way to fall.
- **Below about 14:** there is little fear in the price to lose, and the option is cheaper.

Bought options do best on direction when IV is rising. They do worst when IV is already high and about to fall, which is exactly the condition at 9:15 AM after an anxious night.

## What this note does not claim

The levels of 20 and 14, and the window of 5 to 15 minutes, are working rules of thumb. They are not the result of a published AION test and no hit rate is claimed for them. IV does not fall after every open. On a morning when the news gets worse after 9:15 AM, IV can keep rising and the same Put gains from both delta and vega.

The 40% fall in the opening example is an illustration of scale, not a measured average.

<div class="tags">

<span class="tag">Implied volatility</span><span class="tag">Vega</span><span class="tag">Option premium</span><span class="tag">Opening window</span><span class="tag">India VIX</span><span class="tag">Theta decay</span>

</div>
