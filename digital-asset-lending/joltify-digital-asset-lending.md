# Joltify Digital Asset Lending

<figure><img src="../.gitbook/assets/market (1).png" alt=""><figcaption></figcaption></figure>

## Interest Rate Model

Decentralized finance (DeFi) protocols often use interest rate models to determine the interest rates on borrowed and lent digital assets. These models are typically based on the utilization rate (U) of the assets in a given pool, which is an indicator of the availability of capital within the pool.

As the utilization rate increases, the interest rates on borrowed assets may decrease in order to encourage borrowing and increase liquidity in the pool. Similarly, as the utilization rate decreases, the interest rates on lent assets may increase in order to encourage repayments of debt and additional capital injection into the pool.

Different DeFi lending protocols may use different parameters and calculations to determine the interest rates on borrowed and lent assets. Some protocols may use a fixed interest rate, while others may use a variable interest rate that is based on the utilization rate or other factors.

Overall, the use of interest rate models in DeFi protocols helps to align the liquidity in the pool with the borrowing and lending interest rates, providing a balance between encouraging borrowing and encouraging repayments and additional capital injection.

In Joltify, the parameters in the interest rate model are defined as follows:

BaseRateAPY: &#x20;

The base or Y-intercept rate of annual percentage yield (APY) is the interest rate that is applied when there are no borrows in a given money market. This rate is often used as the starting point for calculating the interest rate on borrowed assets in a money market, and it may be adjusted based on the utilization rate or other factors.

For example, if a DeFi protocol has a base rate of 0.02, this would signify an interest rate of 2% APY as the Y-intercept of the interest rate model for the money market. The interest rate on borrowed assets would then be calculated based on this base rate, as well as the utilization rate and any other relevant factors.

It is important to note that internally, interest rates are typically stored as per-second interest in order to provide greater precision and accuracy. This means that the base rate of APY may be converted into a per-second interest rate before it is used to calculate the interest on borrowed assets.

Kink:

The inflection point is the point at which the base multiplier, which is used to calculate the interest rate on borrowed assets, no longer applies and the jump multiplier begins to apply. This inflection point is often determined by the utilization rate of the assets in a given money market.

For example, if a DeFi protocol has an inflection point of 0.8, this would signify that at 80% utilization, the jump multiplier would begin to apply and the interest rate on lent assets would be calculated using this multiplier, rather than the base multiplier.

The inflection point is an important concept in DeFi protocols, as it helps to balance the liquidity in the money market by encouraging borrowing when capital is available and encouraging repayments and additional capital injection when the utilization rate is high. This can help to maintain a stable and sustainable ecosystem for digital asset lending and borrowing.

&#x20;BaseMultiplier:

The base multiplier is a percentage rate that is used to calculate the interest rate on borrowed assets in a money market. This multiplier is applied to the base or Y-intercept rate of annual percentage yield (APY) and it increases the interest rate on borrowed assets for each percentage increase in borrow utilization.

For example, if a DeFi protocol has a base multiplier of 0.01, this would signify that the APY interest rate on borrowed assets increases by 1% for each additional percentage increase in borrow utilization. So, if the base rate of APY is 2% and the utilization rate is 80%, the interest rate on borrowed assets would be calculated as 2% + (0.01 \* 80%) = 2.8% APY.

The base multiplier is an important concept in DeFi protocols, as it helps to align the liquidity in the money market with the borrowing and lending interest rates. By increasing the interest rate on borrowed assets as the utilization rate increases, the base multiplier can help to encourage borrowing and maintain a stable and sustainable ecosystem for digital asset lending and borrowing.

JumpMultiplier:

The jump multiplier is similar to the base multiplier, but it is only applied when the utilization rate of a money market is above the inflection point or "kink". The jump multiplier is used to calculate the interest rate on lent assets, and it increases the interest rate on lent assets for each percentage increase in borrow utilization above the kink point.

The jump multiplier is an important concept in DeFi protocols, as it helps to balance the liquidity in the money market by encouraging repayments and additional capital injection when the utilization rate is high. By increasing the interest rate on lent assets as the utilization rate increases above the inflection point, the jump multiplier can help to maintain a stable and sustainable ecosystem for digital asset lending and borrowing.

The borrowing interest rate R follows this algorithm:

If Utilization Ratio ≤ Kink:



$$
R=UtilizationRation* BaseMultiplier+BaseRateAPY
$$

If Utilization Ratio > Kink:

$$
R= R_{normal} + R_{excess}
$$

$$
R_{nomral}=Kink*BaseMultiplier+BaseRateAPY
$$

$$
R_{excess}=(UtilizationRatio-Kink)*JumpMultiplier
$$

For example, if a DeFi protocol has a  BaseMultiplier of 0.01, a JumpMultiplier of 0.02 and a kink point of 0.8, this would signify that the APY interest rate on lent assets increases by 1% for each additional percentage increase in borrow utilization under 80% and increases by 2% for each additional percentage increase in borrow utlization above 80%. So, if the base rate of APY is 2% and the utilization rate is 90%, the interest rate on lent assets would be calculated as 2% +(0.01\*80%)+ (0.02 \* (90% - 80%)) = 3% APY.

## Digital Asset Lending Terminologies

**Net APY:** The net annual percentage yield (APY) is a measure of the estimated annual return on investment for a given money market, taking into account both the supply and borrow APY of the assets in the market. The net APY reflects the effects of compounding interest on the supply and borrow APY, and it can be used to compare the potential returns of different money markets.

**APY with JOLT:** The APY with JOLT refers to the annual percentage yield that includes any JOLT tokens that may be given as incentives for borrowing or supplying assets in the Joltify platform. This can provide users with additional rewards for participating in the Joltify ecosystem, in addition to the interest earned on their assets.

**Borrow limit:** The amount of money that individuals could borrow from Joltify platform depends on the collateral the individuals deposits.

**Supply Balance:** The amount of money that individuals have deposited into the Joltify platform to earn interests or to borrow other assets. The supply balance is calculated based on all the collateral assets the individual has deposited into the Joltify platform.

**Borrow Balance:** The borrow balance on the Joltify platform is the total amount of money that an individual has borrowed from the platform. This balance is used to determine the individual's borrowable amount, which is the maximum amount of assets that they can still borrow based on their collateral and other borrowed assets.

**Borrowable amount:** The amount of asset an individual can still borrow given the collateral this user has deposited and the other assets this user has borrowed.

**Borrow APY:** The borrow annual percentage yield (APY) on the Joltify platform is the interest rate that users are required to pay when they borrow assets from the platform. This rate is determined by the utilization rate of the assets in the money market and may be adjusted based on the base multiplier and jump multiplier, as well as any other relevant factors.

**Distribution APY:** The distribution annual percentage yield (APY) on the Joltify platform is the interest rate that the platform provides to users as incentives, typically in the form of JOLT tokens. This rate is used to reward users for their participation in the Joltify ecosystem and may vary depending on a variety of factors.

**Daily Earnings:** Daily earnings on the Joltify platform refer to the amount of money that an individual can earn per day in interest, based on the assets that they supply and borrow. This amount is determined by the supply and borrow APY of the assets in the money market, as well as the individual's supply.

