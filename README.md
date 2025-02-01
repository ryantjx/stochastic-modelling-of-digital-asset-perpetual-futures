# Profitability of a Perpetual Instrument
Digital assets offer easy and simple methods to access low leverage trading strategies through perpetuals. These are generally strategies that would replicate a buy-and-hold situation, where you have a long term bullish outlook on the market. However, there are multitudes of solutions and platforms that could be used to optimize this solution.

In this repository, I explore some numerical solutions to find the optimal path that minimizes cost, which mainly comes from Funding Fees.

I will focus on attempting to trade on Hyperliquid as I will be able to provide the live performance of the platform without compromising my wallet address.

## Timeline

## 1 Funding Fees and its affect
### Key Findings
1. Expected Loss from Funding Fees (hourly, 3 months, 50 simulations, pearson distribution)
   1. Ranks
      1. BTC (13950, ): -5.09%
      2. ETH (13950, ): -5.15%
      3. SOL (13950, ): -5.88%
      4. XRP (13950, ): -3.68%
   2. Maybe because there has not been much bullishness in the narrative, the funding fees tend to be less skewed for XRP. As a result, the funding fees being paid for XRP would be significantly lesser compared to ETH and BTC, the mainstays of crypto. SOL has the narrative of being a degen token, as a result, industry is bullish towards SOL, and that is seen in the funding fees being the highest amongst the 4 tokens. 
2. This is a sample of 13950 data points, since July 2023, when Hyperliquid first started. On top of that, the funding mechanism can be quite different for the different platforms. This was also during a bull market period, where the long term trend was linearly positive. I think 3 things might make a significant difference in the funding fees
   1. Platform - certain platforms tend to have extremely different funding rates.
      1. Hourly vs 8 Hourly
      2. Premium Calculation 
   2. Lookback Period - Underlying sample may be different for different time periods. For example, in bear(bull) markets, funding tend to be negatively(positively) skewed. As a result, our lookback period should be similar to the duration that we are simulating for.
      1. Distribution
      2. Size of sample
   3. Liquidity - Low liquidity instruments tend to have fatter tails for funding. In this case, it would be hard to generalize these simulations to those instruments, due to a lack of data. The following methods should be used on larger market cap tokens (BTC, ETH, XRP, SOL), where market manipulation is less likely to occur. 
3. 

## 2 Funding Fees + Volatility

## 3 Funding Fees + Volatility + Premium Spread

## 4 Platform Comparisons - 
