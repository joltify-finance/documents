# Joltify Chain Bridge

To allow the token transfer from and to one public chain (for example, Ethereum chain or Binance smart chain) to Joltify chain, cross chain bridge are employed to allow users to send and receive the token in bi-direction.



### Transferring token from public chain to  Joltify chain

1. User Alice transfers her token to the bridge router on the public chain end.
2. Once Joltify chain validator observes the transfer to the given bridge router end, it will mint the corresponding amount of wrap-tokens to the user’s corresponding Joltify chain address.&#x20;

### Transferring token from Joltify chain to public chain

1. User Bob transfers his token to the bridge router on the Joltify chain end.
2. Once Joltify chain validator observes the transfer to the given bridge router end, it will transfer the corresponding token to Bob address on the public chain.
3. Once the transfer transaction is confirmed on the public chain, the wrap token minted in Joltify chain will be burned

&#x20;

&#x20;
