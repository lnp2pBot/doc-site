# Common problems and their solutions

## I tried to pay an invoice with a wallet with insufficient funds and [@lnp2pbot](https://t.me/lnp2pbot) now tells me that the invoice was used

Wait 15 minutes for the transaction time to expire and start it again for a new invoice to be generated.

## My counterparty had a problem sending me the payment in fiat and then it disappeared, my sats were blocked

The transaction will be automatically canceled after 23 hours and your satoshis will appear in your wallet as a failed payment.

## A user took my purchase by mistake and I already made the payment in satoshis

A cooperative cancellation can be initiated. The initiator must execute the command `/cancel <command identifier>` and the counterpart only needs to run `/cancel` and touch the button to confirm.

## I canceled an order but the sats have not returned to my wallet, how long should I wait?

When an order is canceled, the seller's sats return immediately to the node/wallet that made the payment. If you use a self-custody wallet or your own node you will not have any problem but if you use a wallet that custodies your funds you must wait for them to reflect your balance in their internal system, this can take from a few minutes to a couple of hours depending on the wallet but in all wallets it returns 100% of your funds, be patient.
