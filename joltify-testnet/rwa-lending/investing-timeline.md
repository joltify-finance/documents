# Investing Timeline

## Stages

<figure><img src="../../.gitbook/assets/timeline (1).jpg" alt=""><figcaption><p>Figure 1: The operation timeline including the operations in five stages.</p></figcaption></figure>

As illustrated in Figure 1, the investment process for the RWA project can be delineated into five distinct stages:

* [**The "Pool Preparing" Stage**](investing-timeline.md#the-pool-preparing-stage): allows the SPV to propose the project. This stage primarily aims to capture the community's attention and interest.
* [**The "Investing" Stage**](investing-timeline.md#the-investing-stage): allows users to commence their investments.
* [**The "Borrowing" Stage**](investing-timeline.md#the-borrowing-stage): allows the SPV to commence their borrowing, leveraging the fund accumulated.
* [**The "Interests Accumulating" Stage**](investing-timeline.md#the-interests-accumulating-stage): distributes the amassed interests from the SPV to the respective investors. Concurrently, additional functionalities become accessible to users such as "_Transfer Ownership_".
* [**The "Pool Closing" Stage**](investing-timeline.md#the-pool-closing-stage): necessitates the SPV to settle both the interest and principal amounts to the investors. Subsequent to this, investors are at liberty to withdraw their principal investment along with the accrued interest.

***

## <mark style="background-color:blue;">The "Pool Preparing" Stage</mark>

### >>> Operations of the SPV

1. **Project Addition**
   1. **Proposal Submission**: The SPV must submit a proposal to commence a project on Joltify.
   2. **Documentation**: The SPV needs to prepare essential documentation, such as a Project Introduction.
   3. **Agreement to Terms:** It is imperative for the SPV to accept Joltify's terms and conditions.
   4. **Community Engagement:** An AMA (Ask Me Anything) session should be organised by the SPV for the community's benefit.
   5. **Community Consensus:** The SPV awaits the community's decision through their voting on the proposal.
2. **Pool Management**
   1. **Addition:** The SPV has the capability to establish pools, specifying expected APY(%) and Target Amount($) for the proposed project.
   2. **Modification:** Prior to activation, the SPV can adjust the pool's APY(%) and Target Amount($).
3. **Pool Activation**
   1. The SPV activates pools for users to invest.

### >>> Operations of Investors

1. **Proposal Voting**
   1. JOLT holders have the privilege to cast votes to either accept or reject the project proposed by the SPV.

***

## <mark style="background-color:purple;">The "Investing" Stage</mark>

### >>> Operations of the SPV

1. **Agreement Signing**
   1. The SPV is tasked with verifying and endorsing the investment agreements signed by users.
2. **Permission Granting**
   1. The SPV has the right to either approve or decline investors to invest the proposed project.
3. **Borrow**
   1. The SPV starts borrowing assets from users on this stage. Moreover, the borrowing amount and frequency are constrained by the designated '_target amount_' and '_borrow count_'.

### >>> Operations of Investors

1. **KYC Verification**
   1. Investors must upload their KYC to advance with their investment.
   2. Additionally, linking to their Google Account is mandatory.
2. **Agreement Signing**
   1. Prior to investing, users must sign the provided agreement.
   2. Additionally, they must receive permission from the SPV to initiate their investment.
3. **Invest**
   1. Users authorised by the SPV can deposit the requisite assets into their chosen pool.

{% hint style="info" %}
_Note that the Joltify Testnet Campaign has temporarily suspended the KYC verification process for testing._
{% endhint %}

***

## <mark style="background-color:orange;">The "Borrowing" Stage</mark>

### >>> Operations of the SPV

1. **Borrow**
   1. The SPV can continue borrowing if the '_target amount_' is not met. This can proceed until the specified target amount or the maximum '_borrow count_' is reached.

{% hint style="info" %}
If the SPV fails to undertake any borrowing action during this stage, the project will be automatically rejected, allowing users to immediately withdraw their committed assets.
{% endhint %}

### >>> Operations of Investors

At this stage, users are not required to perform any action.

{% hint style="info" %}
When users commit assets and the SPV borrows them, these users are granted an NFT that encapsulates key investment details, including the borrowed asset amount.
{% endhint %}

***

## <mark style="background-color:green;">The "Interests Accumulating" Stage</mark>

### >>> Operations of the SPV

1. **Repay interests**
   1. The SPV can begin disbursing the accumulated interest from completed payment rounds to the pool.
2. **Borrow**
   1. If the target amount is not reached and there are new investments, the SPV can keep borrowing until the '_target amount_' or the max '_borrow count_' are reached.

### >>> Operations of Investors

1. **Invest**
   1. At this stage, users can continue investing their assets. However, it's important to note that newly deposited assets won't be directly added to the pool. Instead, they'll be designated with a "Committed" status,, waiting to be transited into "Invested" status.
   2. The transition of committed assets from "Committed" status to an "Invested" status occurs in two scenarios:
      1. **Case 1**: If the pool has not reached its target amount and the SPV borrows at this stage, the committed assets of users will be borrowed.
      2. **Case 2**: When ownership transfer requests arise from other users, the committed assets will transition to "Invested" status in the following payment round.
2. **Transfer Ownership**
   1. At this stage, users have the option to transfer ownership of their invested assets. The processing varies based on three distinct scenarios:
      1. **Case 1**: If no assets are committed during the period, any ownership transfer requests will be left unprocessed and the assets will remain "Invested".
      2. **Case 2**: If the total committed assets are 100 USDC (committed) and 20 USDC (invested) is requested the ownership transfer, 20 USDC (out of 20 invested USDC) becomes withdrawable and 80 USDC (out of 100 committed USDC) remains "Committed".
      3. **Case 3**: If the total committed assets are 100 USDC and 150 USDC is requested the ownership transfer, 100 USDT (out of 100 invested USDC) becomes "Invested" and 50 USDC (out of 150 invested USDC) remains "Invested". **Notably**, in this case, new NFTs will be generated for users requesting ownership transfer, as their invested assets haven't been completely transferred.
   2. Please be aware that once a user initiates an ownership transfer request, any of their committed assets will be excluded from the ownership transfer process.
3. **Withdraw**
   1. At this stage, users have the option to withdraw either their committed assets or assets redeemed through ownership transfer requests.
4. **Interest Claim**
   1. Users can claim interest that has been accumulated from previously completed payment rounds, based on their invested assets.
5. **Withdrawal Proposal Submission**
   1. Upon concluding this stage, users have the option to submit a withdrawal request to retrieve their invested assets.\
      The SPV must repay investors' principal/invested assets according to the investor's `withdrawal proposals`. The SPV reserves the right to roll over the investment to the next cycle if no withdrawal proposal is received.

***

## <mark style="background-color:red;">The "Pool Closing" Stage</mark>

### >>> Operations of the SPV

1. **Interest Repayment**
   1. Before closing the pool, the SPV must settle the accumulated interest.
2. **Principal Repayment**
   1. The SPV must repay borrowed assets as per users' withdrawal requests.
3. **Pool Closing**
   1. The SPV can close the pool if and only if all accrued interests  and borrowed assets are settled and returned.

### >>> Operations of Investors

1. **Interest Claim**
   1. Users can claim all accumulated interest at this stage.
2. **Principal Withdraw**
   1. Users can retrieve their invested assets once the SPV has completed the principal repayment.
