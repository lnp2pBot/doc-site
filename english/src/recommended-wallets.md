# Recommended Wallets

The following wallets have shown better performance when used with [@lnp2pBot](https://t.me/lnp2pBot):

- [Breez Wallet](https://breez.technology/)
- [Blixt Wallet](https://blixtwallet.github.io/)
- [Phoenix Wallet](https://phoenix.acinq.co/)
- [@LightningTipBot](https://t.me/LightningTipBot)

#### Notes on other wallets
With `Wallet of Satoshi`, or any other custodial service, it might occur that if you're selling Sats and the order is canceled, your wallet balance might take a while to update, and the Sats might not appear available for some hours, even if they're in the wallet's node. This delay happens because custodial wallets update their users' balances periodically, so you'll have to wait for a few hours.

It's common for payments from [@lnp2pBot](https://t.me/lnp2pBot) to `Muun wallet` to fail because the bot can only pay a maximum routing fee of up to 0.2%. Hence, it might not cover the invoice when Muun charges fees higher than that. In such cases, you'll need to generate a new invoice from another wallet (More info [here](./i-cant-receive.md)). 
It's also possible that if you're selling Sats from Muun wallet and the order is canceled, a fee will still be charged because Muun wallet isn't a native LN wallet; it's an on-chain wallet that operates through submarine swaps. For any transaction, you'll have to pay the mining fee, even if the bot's hold invoice was canceled.
