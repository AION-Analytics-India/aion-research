# Veritas: From Bachelier to Black-Scholes, and Why It Matters for Opening Bands

Published May 5, 2026 · AION Analytics (India) · Lokesh Gupta

Canonical version: <https://aionanalytics.in/research/notes/veritas-bachelier-bsm>

---
AION Veritas publishes daily opening probability bands. This note explains the century-old mathematical lineage behind those bands — from Louis Bachelier's 1900 diffusion insight through Black-Scholes-Merton's option pricing framework — and why that lineage is the right tool for pre-market range estimation.

## Louis Bachelier, 1900

In his 1900 doctoral thesis, Louis Bachelier proposed that price movements in financial markets follow a *random walk* — that each increment in price is drawn from a probability distribution independent of past price history. This was a radical claim at the time, and largely ignored for half a century.

Bachelier's key insight was that the distribution of price changes over a time interval τ follows a Gaussian (normal) distribution with variance proportional to τ. The probability that a price ends up within a specific range after time τ can be computed from the mean and standard deviation of that distribution. This is the foundation of every probability band in financial mathematics.

## The diffusion intuition

Bachelier borrowed the mathematics from physics — specifically from the study of heat diffusion. A drop of ink in water spreads outward from its starting point over time. The probability distribution of where any given ink molecule will be after time τ is a Gaussian centered on the starting point, with spread growing as √τ.

Price behaves similarly. The longer the time interval, the wider the probability distribution. The width grows proportionally to the square root of time, not time itself. This √t scaling is the reason that 30-day implied volatility is not 30 times the 1-day implied volatility — it is √30 ≈ 5.5 times. Every options textbook and every volatility surface in the world embeds this Bachelier insight.

## Black-Scholes-Merton, 1973

Fischer Black, Myron Scholes, and Robert Merton formalised Bachelier's random walk framework into a complete options pricing model. The Black-Scholes-Merton equation gives the fair price of a European option given: current price, strike price, time to expiry, risk-free rate, and implied volatility.

The key addition over Bachelier was the *risk-neutral pricing* framework and the incorporation of continuous-time stochastic calculus (specifically Itô's lemma). This allowed the derivation of a replicating portfolio — a combination of the underlying and cash — that exactly replicates the option payoff, giving a theoretically unique fair price.

From this framework, one can extract the implied distribution of the underlying at expiry. The market price of an option implicitly encodes the probability the market is assigning to different outcomes. This is the option-implied distribution.

## What Veritas does with this

AION Veritas does not attempt to replicate the full BSM pricing machinery. It uses the core probabilistic insight: given today's implied volatility (available directly from India VIX for the Nifty), the time horizon (one trading session, approximately 375 minutes), and adjustments for the current VIX regime and overnight information (GIFT Nifty tape, global cues, event severity), the expected distribution of tomorrow's opening price can be estimated.

The output is a probability band — a range within which the open is estimated to fall with a specified probability. The band is not a price target. It is not a trading signal. It is a quantified expectation of range, using mathematics that has been standard in financial theory since 1973 (and in mathematical physics since 1900).

Publishing this band daily — before the session opens, with the actual open recorded afterward — is a public model validation exercise. The failures are as informative as the successes. A band that contains the actual open 75-80% of the time over a statistically significant sample is performing as the underlying mathematics would predict. A band that contains it 95% of the time is too wide. One that contains it 50% of the time has a miscalibrated scaling factor.

## Why AION publishes validation receipts

Any model that is not publicly validated is not a model — it is a story. The Veritas band history — including every miss, every overestimate, every underestimate — is the evidence base for the model's calibration claims.

This practice traces directly to the <a href="https://ssrn.com/abstract=6449739" target="_blank" rel="noreferrer">Asymmetric Multipolarity paper</a>'s framing of information integrity: the model must be inspectable, bounded, and accountable. A black-box range estimator that never reveals its failures is not providing information — it is providing comforting noise.

<a href="/veritas" class="ssrn-link">View Veritas validation receipts →</a>

<div class="tags">

<span class="tag">Veritas</span><span class="tag">Bachelier</span><span class="tag">Black-Scholes</span><span class="tag">BSM</span><span class="tag">Probability bands</span><span class="tag">Options pricing</span><span class="tag">Stochastic processes</span>

</div>
