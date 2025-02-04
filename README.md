# Profitability of a Perpetual Instrument
Digital assets offer easy and simple methods to access low leverage trading strategies through perpetuals. These are generally strategies that would replicate a buy-and-hold situation, where you have a long term bullish outlook on the market. However, there are multitudes of solutions and platforms that could be used to optimize this solution.

In this repository, I explore some numerical solutions to find the optimal path that minimizes cost, which mainly comes from Funding Fees.

I will focus on attempting to trade on Hyperliquid as I will be able to provide the live performance of the platform without compromising my wallet address.

## Timeline
01/02/2025 - 1_fundingfees.ipynb 
03/02/2025 - 2_fundingandprice.ipynb
04/02/2025 - Hyperliquid Vault Set-up
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

## Live Testing
### Hyperliquid Vault Setup

#### Introduction and Rules
For the purposes of estimating the performance of the portfolio, I decide to use a [Hyperliquid Vault](https://hyperliquid.gitbook.io/hyperliquid-docs/vaults) to ensure visibility and transparency of the portfolio. However, I will not share the details of the vault as it will expose my on-chain identity, which I wish to keep private. The vault's performance will be based on regular updates on this github repository.

The initial setup will be as such
- Position Size: 2x Leverage (With potential to change)
- Asset: BTC (ETH/SOL/XRP)
- Duration: XX FEB 25 - 31 MAR 25

Throughout the duration of the trade, I will not make discretionary trades with the vault, unless necessary (Some of the conditions would be: bankruptcy, getting robbed or any extreme circumstances).

#### Expected Results
Based on the testing, at the end of the duration (given that I only had 2 out of 3 backtested months) would be:
1. Returns: +46% 
2. Percentiles
   1. 95th: +200%
   2. 5th: -20%
3. Liquidation Risk: 0.8%

#### Timeline (Weekly)
| Date | APR (7d) | APR (30d) | Age (days) |
|------|----------|-----------|------------|
|04/02/2025|0%|0%|0|
|10/02/2025|||0|
|17/02/2025|||0|
|24/02/2025|||0|
|03/03/2025|||0|
|10/03/2025|||0|
|17/03/2025|||0|
|24/03/2025|||0|
|31/03/2025|||0|


## Further Development
1. Platform Comparisons
   1. different platforms have different funding mechanisms. 
   2. Would I pay lesser on a platform that charges 8 hourly vs hourly?
