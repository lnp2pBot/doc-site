# The seller released but I don't get the sats to my wallet

Sometimes the bot does not find successful routes to make the payment for different reasons, sometimes because there is simply not a good connection from the origin to the destination but other times it is much more complicated, it can happen that the nodes connected to the destination charge very high fees, @lnp2pBot's node is willing to pay up to 0.2% of the total amount of the operation in routing fee, if this fee is higher the bot simply will not make the payment, some wallets that are not native lightning may charge more than 0.2% when the mempool is congested, those wallets will not be able to be paid by the bot.

Another case is that you do not have `inbound capacity`, I will give you an example, if you use Blixt wallet and in it you have a channel that you just opened, all the money in that wallet would be outgoing, you do not have the capacity to receive, in that case all Payments to that wallet will fail, there are modern wallets such as the Phoenix wallet that solves this problem by indicating that you do not have inbound capacity and offers you to open a new channel, this wallet charges a commission for this.

As a solution [we recommend trying different wallets](./recommended-wallets.md), generate new invoices and give them to the bot so that it tries to send you the payment again.
