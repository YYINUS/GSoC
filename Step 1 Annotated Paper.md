Annotated Paper: COMMODITIES FOR THE LONG RUN

Key Points from Abstract:

-   explores the performance of commodity futures indices over an extended period, dating back to 1877

-   on average, the returns of commodity futures indices have been positive over the long term

-   return premia are associated with both carry and spot returns, commodity returns in different economic states (inflation up/down, expansion/recession) vary mostly due to moves in the underlying spot price

-   economic states are important drivers of commodity returns

-   returns are stronger when commodity markets are backwardated and inflation is up

-   commodity futures returns into a carry component that is adjusted for the cash rate and excess of cash spot returns

-   low correlation to stocks and long-term government bonds

Key Points from Data and Analysis

Theory:

-   Commodity futures returns can be decomposed as the sum of excess of cash spot returns and interest rate adjusted carry

-   Commodity futures returns may be overestimated by simply considering the sum of excess spot returns and interest adjusted carry

-   By the cost of carry model, commodity futures prices are $$
    F_{t,T} = S_t e^{(r - \psi)(T - t)}
    $$ where authors assume the risk-free interest rate $r$ and convenience yield net of storage costs $\psi$ to be constant for simplicity. *Carry* is the opposite of $(r - \psi)$. $S_t$ is the time t spot price of the commodity. $F_{t,T}$ is the futures price with maturity $T$. $r \equiv In(1 + R)$ is the continuously-compounded riskless rate. $\psi \equiv In(1+\Psi)$ is the yield, net of storage costs.

-   By defining $r^{F_r}_{t,t+1} \equiv ln(1+R^{F_r}_{t,t+1})$ and $r^{S}_{t,t+1} \equiv ln(1+R^{S}_{t,t+1})$ as the continuously compounded return on a futures contract with maturity $T$ and the commodity spot return respectively, author has focused on futures returns can be decomposed as the sum of excess of cash spot returns and interest rate adjusted carry.

-   For the interest rate adjusted carry, the literature points to compensation for bearing inventory risk and/or providing liquidity to hedgers, especially during periods of low inventories (see footnote 2). For spot returns, we focus on two potentially offsetting risk premia, namely commodities’ hedge against inflation and exposure to the business cycle.

Data:

-   The data from 1877 to 1951 are manually transcribed from the Annual Report of the Trade and Commerce of the Chicago Board of Trade. After 1951 and before 2012, the futures prices across various contracts are taken from the data vendor Commodity Systems Inc. After 2012, the futures prices are from Bloomberg. For base metals, rolled return series from S&P, Goldman Sachs, and Bloomberg are used.

-   The author constructed the annualized return on each commodity futures using the following procedure. At each month end, Author calculate the return on each contract from the previous month end.For each month, author held the nearest of the contracts whose delivery month is at least two months away.The returns on the contracts held are spliced together on the roll dates. Using the same rolled contract series, authored constructed a rolled price series and calculate the spot returns.

-   There are large differences between arithmetic and geometric mean returns for individual commodities due to their high level of return volatility for individual commodities. 4.5% Arithmatic against 0.5% Geometric

-   The equal-weighted portfolio is meant to capture the average return across commodities at any given point in time.11 The long-short portfolio represents a common active trading strategy, going long the top third most backwardated and short the third least backwardated commodities

-   One concern might be that historical series on the short rate, especially pre U.S. T-bills in 1929, may not represent the risk-free rate.

-   The higher volatility of the spot return suggests that commodity futures returns are fundamentally about commodity price changes, not just carry

-   Commodities have the attractive property that they are positively skewed. Negative skewedness means crushes.

-   Author defined aggregate backwardation as $\frac{1}{N} \sum_{i=1}^{N} \frac{(F_{i,t,T2} - F_{i,t,T1})}{(T2 - T1) \cdot F_{i,t,T1}} > 0$ where $N$ is the number of commodities. $T1$ and $T2$ are the times to maturity, with $T2$ \> $T1$

-   This average level of backwardation theoretically reflects the level of inventories and hedging demand across commodities.

Summary and Implication:

- Sharpe Ratios increase when commoditities are added to the portfolios due to the drop in violatility
