Assignment 1 WriteUp

SECTION 1 : READING

Q: There are thousands of individual risky assets in which HMC can invest. Explain why MV optimization across 1,000 securities is infeasible.

A: Investing across 1,000 securiites is infeasiable mathematically. In MV Optimization, we need to compute the inverse covariance matrix, which will have 1,000,000 entires, resulting in a computationally expensive procedure. Also, small errors in the expected returns or covariances will get amplified when taking the inverse. 

Q: Rather than optimize across all securities directly, HMC runs a two-stage optimization.

    1. They build asset class portfolios with each one optimized over the securities of the specific asset class.
    2. HMC combines the asset-class portfolios into one total optimized portfolio.

    In order for the two-stage optimization to be a good approximation of the full MV-optimization on all assets, what must be true of the partition of securities into asset classes?

A: Within each speciifc asset class, securities should be highly correlated, and between the different asset classes, the asset classes should be less correlated.

Q: Should TIPS form a new asset class or be grouped into one of the other 11 classes?

A: For diversifiaction purposes it could be benficial for TIPS to form a new asset class, as it behaves differently from assets like equities. Unlike other assets, TIPS can provide investors protection against the eroding effects of inflation, which can also lessen the overall risk of the portfolio.  

Q: Why does HMC focus on real returns when analyzing its portfolio allocation? Is this just a matter of scaling, or does using real returns versus nominal returns potentially change the MV solution?

A: A potential reason for why HMC focuses on real returns could have to do with the fact that the the endowment finacnes a portion of Harvard's budget. Thus, HMC would need to account for inflation, as it affects aspects like scholarships and salaries, areas of Harvard's spending. Additionally, our MV solution from lecture focuses on excess returns, so using real returns would be ideal computationally.

Q: The case discusses the fact that Harvard places bounds on the portfolio allocation rather than implementing whatever numbers come out of the MV optimization problem. How might we adjust the stated optimization problem in the lecture notes to reflect the extra constraints Harvard is using in their bounded solutions given in Exhibits 5 and 6?

A: 

Q: Exhibits 5 shows zero allocation to domestic equities and domestic bonds across the entire computed range of targeted returns, (5.75% to 7.25%). Conceptually, why is the constraint binding in all these cases? What would the unconstrained portfolio want to do with those allocations and why?

A: 

Q: Exhibit 6 changes the constraints, (tightening them in most cases.) How much deterioration do we see in the mean-variance tradeoff that Harvard achieved?

A: 
