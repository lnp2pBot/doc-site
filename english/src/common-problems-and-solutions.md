# Common Problems and Solutions

### I'm trying to take an order, but nothing happens

When you press the `Buy Satoshis` or `Sell Satoshis` button on an offer, [@lnp2pbot](https://t.me/lnp2pBot) will respond privately with what you need to do to complete the process.
For the bot to respond to your request, it's necessary to [initialize it](./how-do-i-initialize-the-bot.md) because no bot can open a chat with you initially if you haven't used it before. Open [@lnp2pbot](https://t.me/lnp2pBot) and type the command `/start` or tap the `Start` button, then try taking the order again, return to the bot, and follow its instructions.
- If you were already using the bot and the last time you did so was before March 2023, you need to reinitialize it with the command `/start` because it was reset, and its previous database wasn't preserved.

### I tried to pay an invoice with an insufficiently funded wallet, and now [@lnp2pbot](https://t.me/lnp2pbot) tells me the invoice was used

Wait for 15 minutes for the transaction time to expire, and then initiate it again to generate a new invoice.

### My counterpart had an issue sending me the fiat payment and then disappeared; my sats got stuck

The transaction will automatically cancel after 23 hours, and your satoshis will appear in your wallet as a failed payment. If you want to expedite the process, you can open a dispute with the command `/dispute <order id>`.

### A user mistakenly took my purchase, and I've already made the payment in satoshis

A cooperative cancellation can be initiated. Both parties need to execute the command `/cancel <order id>`.

### I canceled an order, but the sats haven't returned to my wallet. How long should I wait?

When an order is canceled, the seller's satoshis immediately return to the node/wallet that made the payment. If you use a self-custody wallet or your own node, you won't have any issues. However, if you use a wallet that custodies your funds, you'll need to wait for them to reflect your balance in their internal system. This can take from a few minutes to a couple of hours depending on the wallet, but all wallets return 100% of your funds. Patience is key.

### I'm buying, and the bot doesn't ask me for an invoice; instead, it directly connects me with the seller

This happens when you have a lightning address activated. In that case, the purchased satoshis will be sent directly there without asking for a new invoice for each purchase. To check your lightning address, type the command `/settings` within the [bot](https://t.me/lnp2pbot). If you want to deactivate it, type the command `/setaddress off` within the [bot](https://t.me/lnp2pbot).
