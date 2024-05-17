# Recommended Wallets

The following wallets have shown better performance when used with [@lnp2pBot](https://t.me/lnp2pBot):

- [Breez Wallet](https://breez.technology/)
- [Blixt Wallet](https://blixtwallet.github.io/)
- [Phoenix Wallet](https://phoenix.acinq.co/)

#### Notes on other wallets

-Before selling Sats using any Lightning Network wallet (or exchange), make sure to check if it supports the payment of hold invoices (the type of invoices that the bot uses as escrow)

- With `Wallet of Satoshi`, you can receive Sats from a purchase without any issue. However, if you're selling Sats and the order is cancelled, your wallet balance may take some time to update, and the Sats may not appear available until several hours later, even though they remain in the WoS node. This delay is due to WoS updating the balance of its users periodically. A similar situation may occur with any other custodial service, including other wallets and exchanges that support withdrawals on the Lightning Network.

- It's common for payments from [@lnp2pBot](https://t.me/lnp2pBot) to `Muun wallet` to fail because the bot can only pay a maximum routing fee of up to 0.2%. Hence, it might not cover the invoice when Muun charges fees higher than that. In such cases, you'll need to generate a new invoice from another wallet (More info [here](./i-cant-receive.md)). 
It's also possible that if you're selling Sats from Muun wallet and the order is canceled, a fee will still be charged because Muun wallet isn't a native LN wallet; it's an on-chain wallet that operates through submarine swaps. For any transaction, you'll have to pay the mining fee, even if the bot's hold invoice was canceled.

- In `Aqua Wallet`, you can receive Sats from a purchase without any issue, but despite being a self-custody wallet, if you're selling Sats and the order gets cancelled, your wallet balance may take several hours to update (sometimes up to 48 hours) because they have enabled a waiting period for refunding any failed payments.
