# The Pre-Open Auction: Why 9:00 to 9:15 AM Prices Lie

Published October 8, 2026 · AION Analytics (India) · Lokesh Gupta

Canonical version: <https://aionanalytics.in/research/notes/pre-open-auction>

DOI: [10.5281/zenodo.23227412](https://doi.org/10.5281/zenodo.23227412) (version 2, corrected October 8, 2026)

---
Between 9:00 and 9:15 AM the screen shows prices that no one has traded at. The index figure is indicative while orders are collected, and option prices are the previous session's close until the first trade at 9:15 AM.

The pre-open session runs from 9:00 AM to 9:15 AM. During this window the screen shows a price for Nifty and prices for options. It is easy to read them as today's market. For most of the window they are not. Some are estimates worked out from an order book in which nothing has traded yet. Others are simply left over from the previous session.

## What happens between 9:00 and 9:15 AM

The session is a call auction in the cash market. Orders are gathered first and then matched together at one price, so that the day does not begin with a scramble.

- **9:00 to 9:05 AM: order entry, all orders.** Limit orders and market orders can be entered, changed or cancelled. No matching happens. The exchange shows an indicative opening price that moves as orders arrive.
- **9:05 to 9:10 AM: order entry, limit orders only.** New market orders are refused, and market orders already placed can no longer be changed or cancelled. The exchange closes this stage at a random moment between 9:08 and 9:10 AM, so no one can count on the final seconds.
- **9:10 to 9:12 AM: the single match.** The exchange matches the collected orders at one equilibrium price for each stock. That price is the opening price.
- **9:12 to 9:15 AM: buffer.** Orders are carried over to normal trading.
- **9:15 AM: continuous trading begins.** From here every price on the screen is a trade.

This is the schedule in force since September 7, 2026. Before that date, order entry ran from 9:00 to 9:08 AM and matching from 9:08 to 9:12 AM, and many older explanations still give those times.

<div class="diagram">

![Timeline from 9:00 to 9:20 AM. Order entry for all orders from 9:00 to 9:05, limit orders only from 9:05 to 9:10, single match from 9:10 to 9:12, buffer from 9:12 to 9:15, continuous trading from 9:15. The indicative index price moves during collection and is fixed after the match. The option price on screen stays at the previous close until 9:15 and then jumps to its first real trade.](images/pre_open_auction_timeline.svg)

Figure 1. The pre-open session and what each price on the screen means. Schematic, not market data.

</div>

## Why the index price can mislead

Until the match, the index figure is indicative. It is what the opening price would be if the order book stayed exactly as it is at that second. Orders are still being added and withdrawn, some of them large, and the figure can move a long way before the stage closes.

After the match the opening level of the index is known, and that is real information. But it is the result of one auction in the cash market. It says where the stocks opened. It does not say what an option will cost.

## Why the option price is stale

Options are not matched in the pre-open auction. Since December 2025 the exchange also runs a pre-open auction in the derivatives segment, but it covers futures only. Options begin trading at 9:15 AM. Until then the last traded price on the option chain, shown as LTP, is the close of the previous session. On a Monday that is Friday's close.

Suppose the chain at 9:05 AM shows a Put at 55 rupees. That number is stale. It carries nothing about the overnight news, the gap, or the index level that the auction is about to fix. It says nothing about where the Put will open.

India VIX is in the same position. It is computed from the prices of Nifty options, so before 9:15 AM it also reflects the previous session. It reprices when option trading begins, often sharply. The note on the VIX crush describes what tends to happen to implied volatility in the minutes after that.

## A working rule

A market order placed on the strength of a pre-open price is an order at a price that does not exist yet. The India VIX seen at 9:05 AM is not the India VIX that will be there at 9:15 AM. For an option, the only real prices are the ones that print at 9:15 AM and after.

## What this note does not claim

The 55 rupee Put is an invented example. Indicative prices are not worthless. A large gap in the indicative index level is real information about the order book. It is just not a price at which anything has traded, and for an option it is not a quote.

The exchange sets these timings and has changed them before. On a day when trading is halted by a market-wide circuit filter or an outage, the market reopens with a pre-open session whose times are announced that day.

## Sources

- SEBI circular SEBI/HO/47/11/11(3)2025-MRD-POD2/I/2765/2026, January 16, 2026, on the closing auction session and modifications to the pre-open auction session. It sets the pre-open timings used above, effective September 7, 2026. Circulated by the exchange as NSE/CMTR/72394, January 19, 2026.
- NSE circular NSE/FAOP/74970, July 1, 2026, "Modifications in the Pre-Open Call Auction framework", with its FAQ. It gives the earlier and the revised timings side by side and states that the pre-open session in the derivatives segment applies to futures on stocks and indices.
- NSE circular NSE/FAOP/76186, September 4, 2026, confirming the changes live from September 7, 2026.

<div class="tags">

<span class="tag">Pre-open session</span><span class="tag">Call auction</span><span class="tag">Opening price</span><span class="tag">Option chain</span><span class="tag">India VIX</span><span class="tag">Market microstructure</span>

</div>
