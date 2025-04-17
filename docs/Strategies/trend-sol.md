---
title: TrendSOL
sidebar_position: 2
slug: /trend-sol
keywords: [trend following]
---



# TrendSOL {#f8dcd087b60345ebb4e4262f4cf6988b}


**TrendSOL seeks to produce higher returns than a buy-and-hold SOL strategy (HODL) with the same risk.**


## Description


Trend following strategies exploit the persistence of trends in asset prices by going long assets whose prices have been rising and short assets whose prices have been falling.


Trend following has several advantages that make it an attractive strategy for investors:

- _Positive and high risk-adjusted returns._
- _Low correlations to long market exposure._
- _Lower volatility/drawdowns._
- _Positive returns during crypto bear markets (winter)._

### Economic Rationale


Price trends can persist for behavioral as well as risk-based reasons. The effectiveness of the momentum effect is well documented in quantitative finance. Behavioral explanations suggest that investors tend to under-react to new information in the short-term and subsequently chase returns leading to a "bandwagon" or herding effect. Alternatively, risk-based explanations argue that the momentum premium can be explained by macroeconomic risks like liquidity and other macro factors. 


### Methodology {#1d846a0cd0c380aeaf52efca0755794a}

- **Asset universe**: Solana (SOL)
- **Factor construction**: this involves transforming price data into trend factor scores that quantify the strength and direction of an asset's price momentum relative to its past history. The trend factor captures the tendency of assets that have performed well (or poorly) in the past to continue performing well (or poorly) in the future. It is computed using smoothing/filtering techniques by taking the difference between the current price and the price of the asset n periods ago, where n is the lookback window.
- **Signal generation**: once trend factor scores are computed, they are converted into signals (forecasts) with values between -1 and 1 using a mathematical transformation (learner and/or function).
- **Sizing**: positions are sized in order to achieve a desired volatility target. A volatility scaling factor is computed as the volatility target divided by the realized volatility over the past 3 months. The signal is adjusted by the volatility scaling factor.
- **Rebalancing**: daily.
- **Leverage**: customizable. Leverage can be increased to enhance returns, or decreased to reduce risk in-line with investor risk preferences.

### Market Regimes


Trend strategies work well in trending markets, and poorly in directionless markets. Trending markets can often coincide with periods of high volatility and stress in financial markets, also known as crisis alpha. Hence, they can be good diversifiers during bad times for most assets (see diversification below).


## Performance


The historical performance shown represents the average of many simulations across a range of trend-following algorithms and parameters, rather than a single backtest. It provides an unbiased estimate of future performance, avoiding the inflated expectations that often come from overly optimized backtest results. All returns are risk-adjusted to match the asset’s historical volatility.


## Returns {#7bec643efc474cb0aec192e1af6b8efd}


TrendSOL can be added to passive long SOL exposure to enhance risk-adjusted returns. 


![](./trend-sol.1d846a0c-d0c3-80d2-a801-dcae7a894f22.png)


![](./trend-sol.1d846a0c-d0c3-80d8-81a3-e4aaf832ec9c.png)


![](./trend-sol.1d846a0c-d0c3-8082-8704-e3e48ee84730.png)


## Drawdowns {#819a436290c04617b9def2361a532c61}


TrendSOL can reduce drawdowns by up to 20% relative to SOL.


![](./trend-sol.1d846a0c-d0c3-8061-8dac-d99727aa141b.png)


## Diversification {#eac0ab4ec937476bbc55d45767d2fdc6}


TrendSOL has very low correlation to SOL and broader crypto asset exposure, serving as a good portfolio diversifier especially during bear markets.


![](./trend-sol.1d846a0c-d0c3-80c2-91af-e3291891f4e0.png)


![](./trend-sol.1d846a0c-d0c3-80d6-a2f1-e96d026e53c2.png)


## More Information


### Strategist


Internal team


### Trend Following


To learn more about trend following, see Trend Following (coming soon).


### Trend Vault


To deposit in this strategy, go to our vault.


### Tokenized Funds


To learn more about tokenized funds, read [Tokenized Funds - The Next Evolution of Fund Management](/tokenized-funds).

