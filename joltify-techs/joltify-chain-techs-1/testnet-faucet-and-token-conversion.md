# Testnet Faucet & Token Conversion

## Introduction

To develop on the Joltify EVM co-chain (testnet), developers need to obtain some JOLT tokens and convert them from the Joltify Cosmos chain to the Joltify EVM co-chain.

## Request JOLT Testing Token  <a href="#introduction" id="introduction"></a>

Refer to the [documentation](../../joltify-testnet/get-ready.md) to set up your Keplr wallet and obtain JOLT tokens.

## Token Conversion

To develop on the Joltify EVM co-chain, developers are required to convert their JOLT tokens from the Joltify Cosmos chain to the Joltify EVM co-chain.

### Method 1: Convert JOLT token on Testnet

Developers can easily convert JOLT tokens from the Joltify Cosmos chain to the Joltify EVM co-chain using [Joltify Token Conversion Page](https://testnet2.joltify.io/transfer-token).

### Step 1: Navigate to the Token Conversion page&#x20;

### Step 2: Connect your Keplr wallet on the Page

### Step 3: Convert your JOLT tokens

<figure><img src="../../.gitbook/assets/token_conversion.jpg" alt=""><figcaption><p>Token Conversion (from Joltify cosmos chain to Joltify EVM co-chain)</p></figcaption></figure>

As shown in the figure above, select the JOLT token and enter the amount of JOLT tokens you wish to convert. The receiver address will be automatically generated to receive the converted JOLT tokens on the Joltify EVM co-chain.

### Method 2:

Developers can also convert JOLT tokens via Joltify cmd-line tool as shown below.

```
// joltify tx evmutil convert-cosmos-coin-to-erc20 [initiator pubkey]  [receiver_0x_address] [amount] [flags]
joltify tx evmutil convert-cosmos-coin-to-erc20 \
029165eaba82480df732ede907cc3cfa4db692f0dc572909a33f3237bf8a955471 \ 
0xc65B85A4c0F451bB7d283aD6462cB7A144541839 \
100000000000ujolt --from brian --gas 8000000 
```

