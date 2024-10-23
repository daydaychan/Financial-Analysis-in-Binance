**Long/Short Funding Rate Strategy**


**Introduction**
This strategy uses the funding rate as an indicator to adopt a market-neutral approach. 

**Models for Strategy**
Simple Ranking based on funding rates
Rank their funding rates, short the high ranks, and long the low ranks.
Z-Score model:
Apply the Z-score to normalize funding rates and trade only outside the Z-score threshold.
Deviation from Moving Average:
Calculate the deviation from its moving average to identify extreme values.
Robust Scaling:
Standardize based on the median and interquartile range.
Min-Max Scaling:
Normalize by scaling them to a fixed range → Ensure comparability.
Percentile Normalization:
Normalize funding rates based on their percentile value. 
Rate of Change (ROC):
Measure the relative change over time, to identify tokens with significant recent shifts.

**Universal Value Selection:** Based on Quarterly Market Cap

**Date Fetched:**
2020/4, 2020/8, 2020/12, 2021/4, 2021/8, 2021/12, 2022/4, 2022/8, 2022/12, 2023/4, 2023/8, 2023/12, 2024/4

**Data Source:**
Market Cap information sorted by CoinMarketCap

**Fetching Process**
**Market Cap Sorting:**
Retrieve market cap rankings from CoinMarketCap every quarter from 2020/4 to 2024/4.

**Save Symbols:**
    Store the sorted token symbols in a list.

**Fetch Funding Rates:**
Use the Binance API to collect funding rates for the tokens in the list.

**Data Structure:**
    Organize the fetched funding rate data appropriately.
