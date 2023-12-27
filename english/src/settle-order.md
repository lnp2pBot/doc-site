# Completing an Order

Many disputes arise because one of the parties took too long to respond to a message, there was a misunderstanding, or there was a delay in a payment. These are straightforward cases that only require patience and better communication.
Other cases involve malice, such as when a seller intends to keep the fiat money and reclaim the Sats. For these situations, the solver can execute the `/settleorder` command, which acknowledges the received payment and automatically sends the Sats to the buyer.

![Completing an Order](./assets/images/settleorder.png)

## Completing an Order When Fiat Takes Too Long to Arrive
With [@lnp2pbot](https://t.me/lnp2pBot), users should utilize payment methods that ensure instant fiat transfers. However, there might be instances where fiat takes longer than usual to reach the Sats seller, for example, due to payment processing issues by the bank.
In such situations, the buyer faces the risk of the seller not receiving the fiat [before the hold invoice expires](./how-long-does-it-take-to-finalize-a-transaction.md), thus not releasing the Sats. Once it expires, the seller regains the Sats and then the fiat. The buyer is then dependent on the seller's goodwill, who may or may not send the Satoshis, with no bot intervention possible. To avoid this, users can turn to solvers in their community to act as mediators.

A solver can make the bot freeze the seller's hold invoice using the `/freezeorder <order_id>` command. This allows enough time for the fiat to arrive, and once it does, the solver can release the Sats with the `/paytobuyer <order_id>` command. The buyer's invoice might have expired during this process, requiring an update by typing `/setinvoice <order id> <lightning invoice>`.

This solution involves the bot's custody of the Sats and should be used only when no other options are available.
