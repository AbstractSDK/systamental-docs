---
title: TrendETH
sidebar_position: 2
slug: /trend-eth
keywords: [trend following]
---



# TrendETH {#546ec113b8a64e738a0647b882058428}


**TrendETH seeks to produce higher returns than a buy-and-hold ETH strategy (HODL) with the same risk.**


## Description


Trend following strategies exploit the persistence of trends in asset prices by going long assets whose prices have been rising and short assets whose prices have been falling.


Trend following has several advantages that make it an attractive strategy for investors:

- _Positive and high risk-adjusted returns._
- _Low correlations to long market exposure._
- _Lower volatility/drawdowns._
- _Positive returns during crypto bear markets (winter)._

### Economic Rationale


Price trends can persist for behavioral as well as risk-based reasons. The effectiveness of the momentum effect is well documented in quantitative finance. Behavioral explanations suggest that investors tend to under-react to new information in the short-term and subsequently chase returns leading to a "bandwagon" or herding effect. Alternatively, risk-based explanations argue that the momentum premium can be explained by macroeconomic risks like liquidity and other macro factors. 


### Methodology {#1d846a0cd0c380a1b058e8c4a3298e57}

- **Asset universe**: Ether (ETH)
- **Factor construction**: this involves transforming price data into trend factor scores that quantify the strength and direction of an asset's price momentum relative to its past history. The trend factor captures the tendency of assets that have performed well (or poorly) in the past to continue performing well (or poorly) in the future. It is computed using smoothing/filtering techniques by taking the difference between the current price and the price of the asset n periods ago, where n is the lookback window.
- **Signal generation**: once trend factor scores are computed, they are converted into signals (forecasts) with values between -1 and 1 using a mathematical transformation (learner and/or function).
- **Sizing**: positions are sized in order to achieve a desired volatility target. A volatility scaling factor is computed as the volatility target divided by the realized volatility over the past 3 months. The signal is adjusted by the volatility scaling factor.
- **Rebalancing**: daily.
- **Leverage**: customizable. Leverage can be increased to enhance returns, or decreased to reduce risk in-line with investor risk preferences.

### Market Regimes


Trend strategies work well in trending markets, and poorly in directionless markets. Trending markets can often coincide with periods of high volatility and stress in financial markets, also known as crisis alpha. Hence, they can be good diversifiers during bad times for most assets (see diversification below).


## Performance


The historical performance shown represents the average of many simulations across a range of trend-following algorithms and parameters, rather than a single backtest. It provides an unbiased estimate of future performance, avoiding the inflated expectations that often come from overly optimized backtest results. All returns are risk-adjusted to match the asset’s historical volatility.


### Returns {#1d746a0cd0c3807384dadb782665464b}


TrendETH can be added to passive long ETH exposure to enhance risk-adjusted returns. 


![](./trend-eth.1d846a0c-d0c3-8038-a6c2-ffe03e7df1a0.png)


![](./trend-eth.1d846a0c-d0c3-8016-bb22-eea6dce666b3.png)


![](./trend-eth.1d846a0c-d0c3-8042-bb76-d4aa22f4220e.png)


### Drawdowns {#1d746a0cd0c380c4913cd447d519ecc7}


TrendETH can help reduce drawdowns especially during bear markets.


![](./trend-eth.1d846a0c-d0c3-80c7-bb7b-c386de47cca6.png)


### Diversification {#1d746a0cd0c380269cd3dcab1c076a72}


TrendETH has very low correlation to ETH and broad crypto asset exposure, serving as a good portfolio diversifier especially during bear markets.


![](./trend-eth.1d846a0c-d0c3-8033-8d42-d687b8820588.png)


![](./trend-eth.1d846a0c-d0c3-8078-bb80-f8cf26377a7f.png)


## More Information


### Strategist


Internal team


### Trend Following


To learn more about trend following, see Trend Following (coming soon).


### Trend Vault


To deposit in this strategy, go to our vault.


### Tokenized Funds


To learn more about tokenized funds, read [Tokenized Funds - The Next Evolution of Fund Management](/tokenized-funds).

