## YEYUXI YI Test Results - Expected Returns

1.  Pre-req :

    <https://github.com/YYINUS/Market-Efficiency-Test>

    A research on the market efficiency after the announcement of earnings reports

2.  Easy :

    The packages are initially saved as tempo files since I didn't have Rtools. I solved the issue by installing Rtools into my computer.

3.  Intermediate :

    See Private Message

4.  Hard

    **Investment horizons**

    For XRET.EW(Equal-Weighted Portfolio Returns)

    -   The coefficients for **`USREC`** and **`INFL.STATE`** are statistically significant at the 0.05 level or better in the horizon 0 (**`H0`**) model, indicating a relationship between these variables and equal-weighted portfolio returns in the short term.

    -   The significance of the coefficients suggests that periods of U.S. recession (**`USREC`**) are negatively associated with commodity portfolio returns, whereas inflation state (**`INFL.STATE`**) shows a positive association.

    -   In longer horizons (**`H11`** and **`H59`**), the predictive power of these variables diminishes, as indicated by the lack of statistical significance in those coefficients ( higher than 0.05 level )

    For XRET.LS (Long-Short Portfolio Returns)

    -   The coefficients for **`USREC`** , **`INFL.STATE`** and **`PFC.STATE`** are statistically insignificant at the 0.05 level or better in the horizon 0 (**`H0, H11 and H59`**) model, indicating there is no conclusive evidence that the periods of U.S recession(**`USREC`**), inflation state(**`INFL.STATE`**) and state of the future market(**`PFC.STATE`**) affect Long-Short Portfolio Returns portfolio returns in the both short term and long term.

    Investment Styles

    For XRET.EW(Equal-Weighted Portfolio Returns)

    -   The coefficient for **`MoM.EW`** is statistically significant at the 0.05 level or better in the horizon 0 (**`H0`**) model, indicating there is a relationship between the momentum investment style and the return of the equal-weighted portfolio returns in the short term.
    -   In longer horizons (**`H11`** and **`H59`**), the predictive power of **`MoM.EW`** diminishes, as indicated by the lack of statistical significance in those coefficients ( higher than 0.05 level )
