# Expiry Week Mechanics: Why Tuesday Is Not Like Friday

Published October 8, 2026 · AION Analytics (India) · Lokesh Gupta

Canonical version: <https://aionanalytics.in/research/notes/expiry-week-mechanics>

DOI: [10.5281/zenodo.23227415](https://doi.org/10.5281/zenodo.23227415) (version 2, corrected October 8, 2026)

---
Nifty weekly options expire on Tuesday. The day before and the morning of expiry do not behave like the rest of the week, because time decay speeds up and the contest around Max Pain is settled in a few hours.

The Nifty weekly contract now expires on Tuesday. The National Stock Exchange moved its expiry day from Thursday to Tuesday for contracts expiring on or after September 1, 2025, after SEBI limited the days on which equity derivatives may expire. Every week therefore has a Tuesday on which all Nifty weekly options stop existing. The sessions that lead up to that moment do not behave like the rest of the week.

## The sequence

- **Monday.** Theta decay accelerates. Theta is the premium an option loses for each day that passes, and it grows as expiry gets closer. Options that are out of the money lose premium fast.
- **Tuesday morning.** The final gamma contest. The desks that have written options try to keep spot pinned near Max Pain. If they succeed, most options expire worthless.
- **Tuesday afternoon.** Expiry and settlement. All open positions in the weekly series are settled in cash at the final settlement price, which is based on the closing value of the index on expiry day. Positions for the next week are opened.

<div class="diagram">

![Timeline of an expiry week in three stages. Monday: the premium of an out-of-the-money option falls along a steepening curve. Tuesday morning: a tug of war between desk pinning toward Max Pain and the trader's directional bet. Tuesday afternoon: a settlement document with a tick. A note reads: the window is short, theta is the clock.](images/expiry_week_timeline.svg)

Figure 1. The last two sessions of a Nifty weekly contract. Schematic, not market data.

</div>

## Why Monday is expensive

Time decay is not spread evenly over the life of an option. An option with thirty days left loses a small part of its time value each day. An option with one day left loses nearly all of what remains. The curve steepens at the end.

For the buyer this changes what a day of waiting costs. On a Thursday, holding an out-of-the-money option overnight is cheap. On a Monday before a Tuesday expiry, the same wait can cost most of the premium, even when the index does not move at all.

## Why Tuesday morning is a contest

On expiry morning the options close to spot have very little time value left, and their delta changes quickly with every small move in the index. This is what high gamma means. A move of a few points can turn a worthless option into a valuable one, or the reverse.

The writers want spot to finish where they pay out the least, which is near Max Pain. Directional traders want it to finish somewhere else. For a few hours the two sides pull against each other in a narrow range. The note on Max Pain explains how the pin is held and what breaks it.

## Why this matters

A trader who holds a bought option into expiry week is not only betting on direction. The bet is that the direction arrives before theta has taken the premium. The window is short. The desks that write options know this, and time is on their side.

## What to look at

1. **The theta value on the option chain.** It shows what one more day of holding costs, in rupees.
2. **The distance between spot and Max Pain on Monday.** A small distance favours the pin. A large one means the writers have ground to recover and little time.
3. **The change in OI on Tuesday morning.** If open interest is falling quickly at a strike, the writers there are unwinding. A pin that is being unwound is close to breaking.

## What this note does not claim

The expiry day is set by the exchange and has changed before. A Tuesday that is a trading holiday moves the expiry; by long-standing practice it moves to the previous trading day, but the contract specification for that week is the authority. Check it before relying on the day named here.

How the closing value itself is formed has also changed. Until August 2026 the closing price of a stock was the volume-weighted average of its last thirty minutes of trading. From August 3, 2026 the closing price of stocks that have derivatives is set in a closing auction after 3:15 PM. This note does not describe the settlement calculation in detail.

The three readings are working rules of thumb. They are not the result of a published AION test, and no hit rate is claimed for them. Pins fail on ordinary days and hold on eventful ones.

## Sources

- NSE circular NSE/FAOP/68589, June 17, 2025, "Revision in Expiry Day of Index and Stock derivatives contracts": Tuesday for contracts expiring on or after September 1, 2025, with monthly contracts on the last Tuesday of the month. It refers to SEBI circular SEBI/HO/MRD/TPD-1/P/CIR/2025/76, May 26, 2025.
- NSE circular NSE/FAOP/68747, June 25, 2025, with the revised expiry dates contract by contract.
- SEBI circular SEBI/HO/47/11/11(3)2025-MRD-POD2/I/2765/2026, January 16, 2026, and NSE circular NSE/CMTR/73362, March 18, 2026, on the closing auction session and how closing prices are set.

<div class="tags">

<span class="tag">Weekly expiry</span><span class="tag">Theta decay</span><span class="tag">Max Pain</span><span class="tag">Nifty options</span><span class="tag">Settlement</span><span class="tag">Open interest</span>

</div>
