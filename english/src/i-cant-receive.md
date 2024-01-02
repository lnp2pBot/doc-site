# The seller released, but I haven't received the Sats in my wallet
## Possible Causes
Sometimes, the bot cannot find successful routes to make the payment for various reasons. It could be due to a poor connection between the origin and destination, or it can be more complicated, such as nodes connected to the destination charging very high fees.

The [@lnp2pBot](https://t.me/lnp2pBot) node is willing to pay up to 0.2% of the total transaction amount in routing fees. If this fee is higher, the bot simply won't make the payment. Some non-native Lightning wallets might charge more than 0.2% when the mempool is congested, and the bot won't be able to pay them (more information on wallets [here](./recommended-wallets.md)).

Another scenario could be that you lack 'inbound capacity.' For instance, if you're using the Blixt wallet and have just opened a channel, all the funds in that wallet would be outbound, and you wouldn't have the capacity to receive. In this case, all payments to that wallet will fail. Modern wallets like Phoenix wallet address this by indicating the lack of inbound capacity and proposing channel modifications ([splice in](https://bitcoinops.org/en/topics/splicing/)) to ensure the new received payment is on the user's side (more inbound capacity). This wallet charges a fee for this service.

## Solution
When a payment fails, the bot will attempt to make the payment two more times with 5-minute intervals. If it continues to fail, the bot will ask you to provide a new invoice to continue trying. It's advisable to generate this invoice from another [wallet](./recommended-wallets.md).

If you don't input the invoice within 20 minutes after the bot requests it, that assistant will be canceled, and it won't request it again later. In that case, you should input it using the command:
`/setinvoice <order id> <lightning invoice>` 
(Do not include the symbols <>, separate each part with a space, and do not reuse invoices).

If you've tried several times and still haven't received the Sats, stay calm. It's no longer possible to cancel the transaction or return the Sats to the seller. Instead, they are in the bot's node, and you can continue trying with new invoices as many times as necessary until you receive them.
