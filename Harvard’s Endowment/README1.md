Assignment 1 WriteUp

SECTION 1 : READING

Q1: There are thousands of individual risky assets in which HMC can invest. Explain why MV optimization across 1,000 securities is infeasible.

A1: Investing across 1,000 securiites is infeasiable mathematically. In MV Optimization, we need to compute the inverse covariance matrix, which will have 1,000,000 entires, resulting in a computationally expensive procedure. Also, small errors in the expected returns or covariances will get amplified when taking the inverse, leading to overfittng. Implementing the resulting weights for all the assets would be impractical in reality, since frequent rebalancing would face high transaction costs and liquidity constraints.

Q2: Rather than optimize across all securities directly, HMC runs a two-stage optimization.

    1. They build asset class portfolios with each one optimized over the securities of the specific asset class.
    2. HMC combines the asset-class portfolios into one total optimized portfolio.

    In order for the two-stage optimization to be a good approximation of the full MV-optimization on all assets, what must be true of the partition of securities into asset classes?

A2: Within each specific asset class, securities should be highly correlated, and between the different asset classes, the asset classes should be less correlated.

Q3: Should TIPS form a new asset class or be grouped into one of the other 11 classes?

A3: For diversifiaction purposes it could be benficial for TIPS to form a new asset class, as it behaves differently from assets like equities (as shown in Exhibit 4). Unlike other assets, TIPS can provide investors protection against the eroding effects of inflation, which can also lessen the overall risk of the portfolio.  

Q4: Why does HMC focus on real returns when analyzing its portfolio allocation? Is this just a matter of scaling, or does using real returns versus nominal returns potentially change the MV solution?

A4: A potential reason for why HMC focuses on real returns could have to do with the fact that the the endowment finacnes a portion of Harvard's budget. Thus, HMC would need to account for inflation, as it affects aspects like scholarships and salaries, areas of Harvard's spending. Additionally, our MV solution from lecture focuses on excess returns, so using real returns would be ideal computationally.

Q5: The case discusses the fact that Harvard places bounds on the portfolio allocation rather than implementing whatever numbers come out of the MV optimization problem. How might we adjust the stated optimization problem in the lecture notes to reflect the extra constraints Harvard is using in their bounded solutions given in Exhibits 5 and 6?

A5: The constraints in the original optimization problem are:

$$
\begin{aligned}
\quad & w^{\top} \mu = \mu_p, \\
& \mathbf{1}^{\top} w = 1.
\end{aligned}
$$

To transform the problem into a bounded quadratic programming problem, we should add a lower and upper limits for each asset class weight. The additional constraints for Exhibit 5 should be: 

$$
\begin{aligned}
0 \leq w_i \leq 1, \quad \forall i \neq \text{cash}, \\
-0.5 \leq w_{\text{cash}} \leq 1.
\end{aligned}
$$

And the additional constriants for Exhibit 6 should be:

$$
\begin{aligned}
w_i^{\text{policy}} - 0.10 \leq w_i \leq w_i^{\text{policy}} + 0.10, \quad \forall i \neq \text{TIPS}, \\
0 \leq w_{\text{TIPS}} \leq 1.
\end{aligned}
$$

Q6: Exhibits 5 shows zero allocation to domestic equities and domestic bonds across the entire computed range of targeted returns, (5.75% to 7.25%). Conceptually, why is the constraint binding in all these cases? What would the unconstrained portfolio want to do with those allocations and why?

A6: The constraint is binding because domestic equities and domestic bonds' risk-adjusted returns are dominated by other asset classes, so the models allocate 0 weights to them. The unconstrained optimization would have assigned negative weights to these assets. Conceptually, the model prefers to short those domestic assets and use the proceeds to invest in more efficient assets such as TIPS, private equity, and commodities.

Q7: Exhibit 6 changes the constraints, (tightening them in most cases.) How much deterioration do we see in the mean-variance tradeoff that Harvard achieved?

A7: From Exhbit 5 to Exhibit 6, the Sharpe ratios decrease from 0.38 to 0.35 or 0.36, indicating a decline in the optimization performance of approximately 9%. 
