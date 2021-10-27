# JOLTIFY Chain Techs

JOLTIFY is the Byzantine Fault Tolerance (BFT) based proof-of-stake public blockchain that is built on the Cosmos digital ecosystem. Joltify has a robust transaction throughput while preserving the safety of the assets within our chain.

The Joltify chain is built on 11 active validators which generate and broadcast the blocks to the network. Validators who participate in the block generation will be paid by the transaction fee plus the incentives emitted from the Joltify project. We anticipate there will be a need to have more active validators, as the demand for Joltify increases.

The selection of the validators is based on the total JOLT they staked plus the age of the validation. The details of the validators election can be found in the section [here.](validator-election-and-punishment.md)

To maintain the health and longevity of the JOLTIFY chain, a punishment policy is introduced to the system to penalize the validators that perform negatively within the JOLTIFY chain. The misbehavior of the validators may be sent to 'jail' (which will stop them from incurring the JOLTIFY chain rewards) for a certain amount of time or even lose a portion of their total sums deposited and the ability to use our platform.

JOLTIFY also welcomes investors who do not have enough JOLT to run a validator. These nodes can delegate their JOLTIFY to one of the active validators and get the JOLTIFY rewards once their delegated validators are participating within our JOLTIFY ecosystem.

### Key terminologies:

**Active Validators:** Active validators are the nodes participants in the block generation.

**Candidate Validators:** Candidate validators are the nodes that maybe choose to be the validators in the coming validator election.

**Inactive Validators:** Inactive validators are the nodes that are ineligible to participate in the Joltify block generation.

In each churn round, the voting power of the validator is calculated as follows:

$$
voting power = permanent power + temporary power
$$

**Temporary power:** Is the value that is reduced based on the age of a validator. For all the validator candidates, the initial temporary voting power for all the nodes is the same. Each churn round, the temporary voting power of an active validator is deducted with a given digit. Once a validator is kicked out from the active validator set, its temporary power will be reset.

**Permanent power:** Is the value calculated based on the staking of a given node. It will not be affected by the transferring of the validator status. The permanent power is updated according to the updates of the validators' staking balance.

**Slashing Point:** Is a mechanism that is built within the proof of stake blockchain protocol, that then discourages the misbehavior. Slashing is essentially designed to incentivize nodes that are secure, available and participating within the network.

Each Churn, all the of the validators voting power will be calculated, the top 11 nodes will be the active validators that participant in the block generation while the rest of the candidates need to wait for the next churn.
