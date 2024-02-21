# Completing an Order

Many disputes arise because one of the parties took time to respond to a message, there was a misunderstanding, or there was a delay in a payment. These are straightforward cases that only require patience and assistance in communication.

Other cases involve malicious intent, such as when a seller wants to keep the fiat money and get the sats returned. In these cases, the solver can execute the `/settleorder` command, which recognizes the received payment and automatically sends the sats to the buyer.

![Completing an Order](./assets/images/settleorder.png)

## Completing an Order When Fiat Takes Too Long to Arrive
With [@lnp2pbot](https://t.me/lnp2pBot), payment methods ensuring instant fiat transfer should be used. However, there might be instances where the fiat takes longer than usual to reach the sat seller, for example, due to issues in payment processing by the bank.
In such situations, the buyer risks the possibility that the seller does not receive the fiat [before the hold invoice expires](./how-long-does-it-take-to-finalize-a-transaction.md), hence not releasing the sats. However, once it expires, the seller will have the sats again, followed by the fiat. The buyer would then be at the mercy of the seller's goodwill, who might or might not send the satoshis, without any bot intervention. To prevent this, users can turn to the solvers in their community to act as mediators.

A solver can make the bot charge the hold invoice from the seller using the `/freezeorder <order_id>` command. This way, they can wait long enough for the fiat to arrive, and when it does, the solver will release the sats using the `/paytobuyer <order_id>` command. The buyer's invoice may have expired during the process, so they'll need to update it by typing `/setinvoice <order id> <lightning invoice>`.

This solution implies custody of the sats by the bot and should only be used when no other options exist.
