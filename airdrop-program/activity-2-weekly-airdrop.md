# (Activity 2) Weekly Airdrop

## Overview

Joltify Team also plans to reward all participants, who are actively interacting with the Joltify network, in a weekly manner.&#x20;

Specifically, the Joltify Team will reward users with cJOLT tokens based on the number of their sent transactions, which interact with Joltify's **Swap**, **Lending**, and **RWA** modules.&#x20;

For more details, you can refer to [_**Ranking**_](activity-2-weekly-airdrop.md#ranking) _**&**_ [_**Rewarding**_](activity-2-weekly-airdrop.md#rewarding).

***

## Ranking

Based on the transaction sent by the jolt-address, the Joltify Team will reward the TOP jolt-addresses (except Joltify's official addresses), who actively interact with the Joltify network, with cJOLT tokens.

### >>> Ranking 1: The SWAP King

"<mark style="color:green;">**The SWAP King**</mark>" indicates the user who sent most transactions to interact with Joltify's `third_party/swap` module.

Specifically, transactions with the following `msgType` are considered in this ranking:

<pre><code><strong>Module:
</strong><strong>    joltify.third_party.swap
</strong><strong>MsgType:
</strong><strong>    - MsgDeposit
</strong><strong>    - MsgWithdraw
</strong><strong>    - MsgSwapExactForTokens
</strong><strong>    - MsgSwapForExactTokens
</strong></code></pre>

### >>> Ranking 2: The LENDING King

"<mark style="color:green;">**The LENDING King**</mark>" indicates the user who sent most transactions to interact with Joltify's `thidr_party/jolt` module

Specifically, transactions with the following `msgType` are considered in this ranking:

```
Module:
    joltify.third_party.jolt
MsgType:
    - MsgDeposit
    - MsgWithdraw
    - MsgBorrow
    - MsgLiquidate
    - MsgRepay
```

### >>> Ranking 3: The AUCTION King

"<mark style="color:green;">**The AUCTION King**</mark>" indicates the users who sent most transactions to interact with Joltify's `third_party/auction` module

Specifically, transactions with the following `msgType` are considered in this ranking:

```
Module:
    joltify.third_party.auction
MsgType:
    - MsgPlaceBid
    - MsgSurplusAuction
    - MsgDebtAuction
    - MsgCollateralAuction
```

### >>> Ranking 4: The RWA King

"<mark style="color:green;">**The RWA King**</mark>" indicates the user who sent most transactions to interact with Joltify's `spv` Module.

Specifically, transactions with the following `msgType` are considered in this ranking:

```
Module:
    joltify.spv
MsgType:
    - MsgDeposit
    - MsgClaimInterest
    - MsgWithdrawPrincipal
    - MsgSubmitWithdrawProposal
    - MsgTransferOwnership
```



**Winners of each ranking can share a total of **<mark style="background-color:green;">**400,000 cJOLT**</mark>** tokens. A total of **<mark style="background-color:green;">**1,200,000 cJOLT**</mark>** tokens, which is equivalent to **<mark style="background-color:green;">**12,000 JOLT tokens**</mark>**, are awarded in this activity(more details are revealed in** [**Rewarding**](activity-2-weekly-airdrop.md#rewarding)**).**

***

## Rewarding

As aforementioned, a total of <mark style="background-color:green;">**400,000 cJOLT**</mark> tokens are awarded to the Top 3 groups of users in each ranking.

To conduct a fair reward distribution, we take the top three groups of users who send the most corresponding transactions and make sure that users in different groups obtain a distinguishable amount of rewards.&#x20;

Specifically, the reward ratio for users in different groups is fixed at <mark style="color:red;">**5:3:2**</mark>. \
For example, if there is 1 user in each group to share 30 cJOLT tokens, they can obtain 15, 9, and 6 cJOLT tokens.

### A Complex Example

Here is a more complex example for the ranking "The Most Active User":\
As shown below, there are <mark style="color:orange;">**20**</mark> users in different groups to share a total of <mark style="background-color:green;">**400,000 cJOLT**</mark> \
**Group 1** \
&#x20;    \-> There are <mark style="color:orange;">**4**</mark> users and each of them sends _<mark style="color:blue;">100</mark>_ transactions in a week \
**Group 2**\
&#x20;    \-> There are <mark style="color:orange;">**10**</mark> users and each of them sends _<mark style="color:blue;">95</mark>_ transactions in a week \
**Group 3**\
&#x20;    \-> There are <mark style="color:orange;">**6**</mark> users and each of them sends _<mark style="color:blue;">90</mark>_ transactions in a week&#x20;

Assume that users in Groups 1, 2, and 3 can obtain _**x**_, _**y**_, and _**z**_ cJOLT tokens.\
Two equations can be inferred below\
$$\ \ \ \ \ \ \ \ \ \ Equation1: \ \  4x + 10y + 6z = 400000$$\
$$\ \ \ \ \ \ \ \ \ \ Equation 2:\ \ \frac{x}{5} = \frac{y}{3} = \frac{z}{2}$$

Based on the above two equations, _**x**_, _**y**_, and _**z**_ can be calculated:\
$$\ \ \ \ \ \ \ \ \ \ x \approx 32,258.06$$\
$$\ \ \ \ \ \ \ \ \ \ y \approx 19,354.83$$\
$$\ \ \ \ \ \ \ \ \ \ z \approx 12,903.22$$\
As a result, for example, 4 users in Group 1 can obtain around <mark style="background-color:green;">**32,258.06 cJOLT**</mark> tokens.\
On the other hand, if the total distributed cJOLT does not exceed 100,000,000 (i.e., [case 1](airdrop-basis.md#case-1)), <mark style="background-color:green;">**32,258.06 cJOLT**</mark> tokens are equivalent to <mark style="background-color:green;">**322.58 JOLT**</mark> tokens.



