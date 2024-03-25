## YEYUXI YI Test Results - Expected Returns

1.  Pre-req :

    <https://github.com/YYINUS/Market-Efficiency-Test>

    A econometric research on the market efficiency after the announcement of earnings reports

2.  Easy :

    The packages are initially saved as tempo files since I didn't have Rtools. I solved the issue by installing Rtools into my computer.

3.  Intermediate :

    See Private Message

4.  Hard — Commodities-long-run.Rmd

    **Overall**

    F - statistics for all models are statistically significant, indicating they are good models and models as a whole has a significant association with the dependent variable — portfolio returns.

    Adjusted R-squared values are notably low in our models, indicating limited explanatory power for portfolio returns. However, this aspect is secondary in our econometric analysis. Our primary goal is to assess the statistical significance of the independent variables, not to optimize predictive accuracy. Therefore, the low Adjusted R-squared can be overlooked in favor of the insights gained from our significant F-statistics, which confirm the relevance of our models in exploring economic relationships.

    **Economic Indicators**

    For XRET.EW (Equal-Weighted Portfolio Returns)

    -   The coefficients for **`USREC`** and **`INFL.STATE`** are statistically significant at the 0.05 level or better in the horizon 0 (**`H0`**) model, indicating a relationship between these variables and equal-weighted portfolio returns in the short term.

    -   The estimates of the significant coefficients suggest that periods of U.S. recession (**`USREC`**) are negatively associated with commodity portfolio returns, whereas inflation state (**`INFL.STATE`**) shows a positive association.

    -   In longer horizons (**`H11`** and **`H59`**), the predictive power of these variables diminishes, as indicated by the lack of statistical significance in those coefficients ( higher than 0.05 level )

    For XRET.LS (Long-Short Portfolio Returns)

    -   The coefficients for **`USREC`** , **`INFL.STATE`** and **`PFC.STATE`** are statistically insignificant at the 0.05 level or better in the horizon 0 (**`H0, H11 and H59`**) model, indicating there is no conclusive evidence that the periods of U.S recession(**`USREC`**), inflation state(**`INFL.STATE`**) and state of the future market(**`PFC.STATE`**) affect long-short portfolio returns in the both short term and long term.

    **Investment Styles**

    For XRET.EW (Equal-Weighted Portfolio Returns)

    -   The coefficient for **`MoM.EW`** is statistically significant at the 0.05 level or better in the horizon 0 (**`H0`**) model, indicating there is a relationship between the momentum investment style and the return of the equal-weighted portfolio returns in the short term.
    -   The estimates of the significant coefficients suggest the momentum investment style is positively associated with commodity portfolio returns in the short term.
    -   In longer horizons (**`H11`** and **`H59`**), the predictive power of **`MoM.EW`** diminishes, as indicated by the lack of statistical significance in those coefficients ( higher than 0.05 level )

    For XRET.LS (Long-Short Portfolio Returns)

    -   The coefficient for **`MoM.EW`** is statistically significant at the 0.05 level or better in the horizon (**`H0`** and **`H11`**) model, indicating there is a relationship between the momentum investment style and the return of the equal-weighted portfolio returns in the short term and medium term.
    -   The estimates of the significant coefficients suggest the momentum investment style is positively associated with commodity portfolio returns in the short term and medium term.
    -   In long term (**`H59`**), the predictive power of **`MoM.EW`** diminishes, as indicated by the lack of statistical significance in the coefficient ( higher than 0.05 level )
    -   The coefficient for **`PFC.AGG`** is statistically significant at the 0.05 level or better in the horizon (**`H59`**) model, indicating there is a relationship between the carry investment style and the return of the long-short portfolio returns in long term.
    -   The estimates of the significant coefficients suggest the carry investment style is negatively associated with commodity portfolio returns in the short term and medium term.

**Summary**

In the econometric analysis of portfolio returns within the commodities market, we discovered that macroeconomic indicators like U.S. recession periods (**`USREC`**) and inflation states (**`INFL.STATE`**) significantly influence short-term equal-weighted portfolio returns. Specifically, recession periods negatively impact returns, while inflationary periods tend to boost them. However, this significance diminishes over longer horizons, suggesting that immediate economic conditions play a more critical role in affecting returns than longer-term economic trends. Additionally, the momentum investment style (**`MoM.EW`**) demonstrates a positive association with short-term returns, indicating its potential utility in short-term investment strategies. Besides, the carry investment style (**`PFC.AGG`**) demonstrates a negative association with long-term returns, indicating its potential lost in long-term investment strategies. In general, the impact of economic indicators and investment styles becomes less predictive over extended periods, highlighting the complexities of forecasting long-term commodity portfolio returns based on current economic conditions and investment styles.

**Repetitive code** — Which-factors.Rmd

data.all \<- merge(FF6.monthly, Q5.monthly, SY4.monthly, DHS3.monthly, BS6.monthly)

data.all \<- data.all[complete.cases(data.all), vars]

data.qbs \<- merge(BS6.monthly, Q5.monthly)

data.qbs \<- data.qbs[complete.cases(data.qbs), unique(c(q5.vars, bs6.vars))]

Lines of codes are repeated. Can shortened into function that both filter complete cases and merge data set.

For example, a function like data.all \<- mergecomplete(vars, ....(more columns if user wants), data = (FF6.monthly, Q5.monthly, SY4.monthly, DHS3.monthly, BS6.monthly)) can do the work
