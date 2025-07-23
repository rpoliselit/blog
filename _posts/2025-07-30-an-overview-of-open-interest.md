---
layout: post
title: "An Overview of Open Interest"
categories: Finance
tags: [en-us, market analysis, derivatives]
math: true
toc: true
---

The most common contracts traded in the financial markets are [Perpetual Swaps and Future Contracts](https://alphractal.github.io/metrics-docs/futures/) and Option Contracts. These are derivatives based on an underlying asset, such as stocks, commodities, currencies, or cryptocurrencies.

The total number of outstanding futures contracts held by market participants is referred to as _open interest_. It represents the total number of contracts that remain unsettled. Importantly, open interest is **not the sum of both** long and short positions, but rather the total number of contracts on **one side** of the market. This is because for every long position, there must be a corresponding short position. Therefore, open interest reflects the number of active positions, regardless of direction.

The mechanism governing changes in open interest reflects the way derivative contracts are initiated and closed. Each contract consists of two counterparties: a **long position** (anticipating a price increase) and a **short position** (anticipating a price decrease). The net change in open interest depends on the nature of the transaction, and it can occur in three distinct ways:

- **Increase** – when both buyer and seller initiate new positions (i.e., a new contract is created), resulting in capital inflow into the market.
- **No change** – when one participant opens a new position while the other closes an existing one, resulting in no net effect on open interest.
- **Decrease** – when both participants close existing positions, leading to a reduction in open interest and capital outflow from the market.

These scenarios are detailed in Table 1.

**Table 1: Impact of Trade Types on Net Change in Open Interest**

| Buyer                                 | Seller                                | Net Change in Open Interest |
| ------------------------------------- | ------------------------------------- | --------------------------- |
| Buys new long (open long position)    | Sells new short (open short position) | Increases                   |
| Buys new long (open long position)    | Sells old long (close long position)  | No change                   |
| Buys old short (close short position) | Sells new short (open short position) | No change                   |
| Buys old short (close short position) | Sells old long (close long position)  | Decreases                   |

Open interest is associated with perpetuals, futures, and options markets, as opposed to the spot market. In cryptocurrency markets, the open interest metric typically reflects **the aggregate of perpetuals and futures** contracts, given that perpetuals are a subset of futures. Options are less commonly traded in crypto and are often reported separately, with open interest figures broken down by contract type.

It is standard practice to separate open interest data for options from that of perpetual and futures contracts. In the context of options, open interest serves as an indicator of market liquidity, supports a broader array of trading strategies, and is frequently used to produce risk-weighted or exposure-weighted analyses.

## The relationship between Price and Open Interest

Open interest movements provide insight into the risk exposure of the underlying asset. An increase or decrease in open interest indicates a change in the number of participants or positions—whether speculative or hedging—which may also reflect variations in leverage. When compared with price movements, open interest can serve as a form of sentiment analysis, as detailed in Table 2.

**Table 2: Market Strength Based on Price and Open Interest Trends**

| **Price Trend** | **Open Interest Trend** | **Market Interpretation**           |
| --------------- | ----------------------- | ----------------------------------- |
| Rising          | Rising                  | Strong (bullish confirmation)       |
| Rising          | Falling                 | Weakening (possible short covering) |
| Falling         | Rising                  | Strengthening (bearish positioning) |
| Falling         | Falling                 | Weak (bearish confirmation)         |

When new capital enters the market—either through aggressive buying during an uptrend or through the opening of new contracts (i.e., increasing open interest)—this is typically interpreted as bullish behavior, signaling a strong market.

Conversely, if prices are rising but open interest is declining, this suggests that capital is exiting the market, primarily through short covering. In such cases, short position holders are being forced to close their positions, which can artificially support the price. This scenario is generally interpreted as bearish, indicating that the underlying market strength is weakening.

If new money flows into the market while prices are in a downtrend, this indicates the presence of aggressive short selling. In such a case, open interest increases as new bearish positions are opened, strengthening the likelihood that the price downtrend will persist. This reflects a bearish outlook, but one supported by increasing market participation.

However, if prices are declining and open interest is also decreasing, this suggests that market participants—particularly long holders—are being forced to liquidate. Capital is flowing out of the market, and this reinforces a bearish interpretation. In such a context, the market is considered weak due to the simultaneous price and participation decline.
 
## Open Interest Delta

The term delta typically refers to the difference in a quantity between two time periods. For open interest, it is defined as:

$$
\text{IO Delta} \equiv \Delta \text{IO} = \text{IO}_\text{current period} - \text{IO}_\text{previous period}
$$

Since open interest represents the total number of active contracts measured at the end of each trading day, the magnitude of the delta reflects market activity or volatility, while its sign indicates the direction of change:

- positive ($$\Delta \text{IO}>0$$) – open interest is increasing, meaning new contracts are being opened,
- negative ($$\Delta \text{IO}>0$$) – open interest is decreasing, indicating that existing contracts are being closed or settled.

While daily deltas are commonly used, this metric can be computed over different time intervals for broader trend analysis, such as 7-day (weekly), 30-day (monthly), 90-day (quarterly), or 180-day (biannually) deltas.

## Volume and Open Interest

Volume refers to the number of contracts traded, counting both when a contract is opened and when it is closed. It resets to zero at the beginning of each trading day and accumulates throughout the day. In contrast, open interest is updated daily and reflects the total number of outstanding contracts that remain open.

This distinction allows for two types of analysis:

- **Intraday analysis** – Useful for assessing absorption and exhaustion, identifying traps (false breakouts), validating short-term trends, and supporting event-driven trading strategies such as day trading and scalping.
- **Interday analysis** – Useful for developing a broader view of hedge fund and institutional investor behavior, identifying accumulation or distribution phases, validating macro trends, and informing long-term strategies such as position or swing trading.

A false breakout—often associated with a short squeeze—can occur when the price breaks a trend with high volume, but open interest declines during the session. This suggests the breakout is not genuine, as market participants are closing positions rather than opening new ones.

When analyzing market behavior across days, volume may be zero, low, or high, while open interest may increase, decrease, or remain unchanged. The interaction between these two metrics provides insight into market dynamics:

- **Zero volume** – Open interest must also be zero; no trading activity has occurred.
- **High volume and rising open interest** – Indicates strong market participation, with a greater number of contracts being opened than closed. This typically reflects increasing investor interest and may signal the initiation or continuation of a prevailing trend.
- **High volume and falling open interest** – Suggests that more contracts are being closed than opened. This behavior may indicate profit-taking, trend termination, or the orderly exit of participants. In cases of sharp price movement, it may also suggest forced liquidations.
- **High volume and stable open interest** – Reflects significant position turnover without net change in the number of open contracts. This may result from position rotation between different market participants (e.g., institutional and retail traders), or signal indecision in a highly liquid environment.
- **Low volume and rising open interest** – Implies limited trading activity, yet with a net increase in open positions. This is generally interpreted as a cautious and gradual market entry, potentially preceding a phase of higher activity.
- **Low volume and falling open interest** – Denotes a gradual reduction in market exposure, with few transactions and declining open positions. This scenario often indicates reduced participation and a cooling or fading market.
- **Low volume and stable open interest** – Indicates a stagnant or range-bound market, with minimal trading activity and no significant change in participants’ positioning.

These scenarios are summarized in Table 3.

**Table 3: Relationship Between Volume and Open Interest**

|**Volume**|**Open Interest**|**Interpretation**|
|---|---|---|
|Zero|Zero|No trading activity.|
|High|Rising|Increasing market interest; trend initiation or continuation.|
|High|Falling|Profit-taking or trend ending; possible forced liquidations.|
|High|Stable|Position rotation or market indecision.|
|Low|Rising|Cautious market entry; potential build-up phase.|
|Low|Falling|Gradual market exit; declining participation.|
|Low|Stable|Stagnant or range-bound market.|

---

1. [Murphy, John J. (1999). _Technical analysis of the financial markets: A comprehensive guide to trading methods and applications_. Penguin. p. 157-179.](https://libgen.li/edition.php?id=136005086)
2. [Kline, Donna (2001). _Fundamentals of the futures market_. McGraw-Hill Professional. p. 142-144.](https://libgen.li/edition.php?id=136068550)
3. [Publication, I. A. E. M. E. (no date) “RELATION BETWEEN OPEN INTEREST AND VOLATILITY IN FUTURES MARKETS.”](https://www.academia.edu/36566801/RELATION_BETWEEN_OPEN_INTEREST_AND_VOLATILITY_IN_FUTURES_MARKETS)
4. [Giagkiozis, I., & Said, E. (2024). Reconciling Open Interest with Traded Volume in Perpetual Swaps. _Ledger_, _9_.](https://doi.org/10.5195/ledger.2024.325)
5. [A Primer on Perpetual Futures](https://www.coinbase.com/en-br/institutional/research-insights/research/market-intelligence/a-primer-on-perpetual-futures)
6. [https://academy.hyblockcapital.com/indicators/orderflow-and-open-interest/open-interest](https://academy.hyblockcapital.com/indicators/orderflow-and-open-interest/open-interest)