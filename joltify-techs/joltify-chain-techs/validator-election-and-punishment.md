# Validator Election & Punishment

Joltify have a dynamic validator set, which means every week, Joltify chain brings new nodes into the validator set while kick out the old nodes.  This gives a fair chance to validates to participants in the block generation. In Joltify, we selected the validators not only base on the user's deposit, but also based on their age as an active validator. &#x20;



### Terminologies:

**Active Validators:** active validators are the nodes participants in the block generation.

**Candidate Validators:** candidate validators are the nodes that maybe choose to be the validators in the coming validator election.

**Inactive Validators:** inactive validators are the nodes that not eligible to participant in the Joltify block generationittar.

In each churn round, the voting power of the validator is calculated as follows:

$$
voting power = permanent power +  temporary power
$$

**Temporary power:**  is the value that reduced based on the age of a validator. For all the validator candidates, the initial temporary voting power for all the nodes is the same. Each churn round, the temporary voting power  of an active validator is deducted with a given digit. Once a validator is kicked out from the active validtor set, its temporary power will be reset.&#x20;

**Permanent power:** is the value that calculated based on the staking of a given node. It will not be affected by the transferring of the validator status. The permanent power is updated  according to the updates of the validators' staking balance.

&#x20;Each Churn, all the validtors voting power will be calculated, the top 11 nodes will be the active validators that participant in the block generation while the rest of the candidates need to wait for the next churn.



### Validator Churn example

As it is shown below, the Joltify chain has the nodes 1 to 8.  For the round **t**, nodes 2, node 3, and node 4 are elected as the active validators, they will be the active nodes that participants in the block generation.

A week later, Joltify will trigger the validator set churn, all the candidates' voting power will be re-calculated, the node2 quit the validator set and node 5 is brought into the validators set. Node 2 will be in the candidate validator set and waiting for the coming churn to join the active validator set again.

![Fig 4 validator election](../../.gitbook/assets/node\_churn.png)

### Validator Punishment

It can be the chance that some validators are not performed correctly, this maybe the node is out of the sync with the blockchain network or some hardware failure.

In Joltify chain, once a node is not perform correct (for example, submitting incorrect block proposal), it will be accumulated with the slashing points. Once the slashing points exceed the threshold, this node will be put in jail for a certain amount of time. If the node still fails to perform correctly, the node has the risk of losing a certain amount of staking jolt.&#x20;

