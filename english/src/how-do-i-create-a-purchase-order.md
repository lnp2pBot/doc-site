# How do I create a purchase order?

The procedure is the same as for the sell order. Only, when pressing the "Menu" button, you must select the command `/buy` instead of `/sell`. This will activate the wizard that will guide you through the buying process.

Once activated, the wizard will ask you to specify the fiat currency with which you want to trade:

![fiat currency](./assets/images/buy-fiat.jpg)

Next, you must enter the amount, in fiat currency, that you want to buy. Remember to enter only numbers in this step, so that the wizard can understand you.

You can also enter a range of amounts to buy, separating the numbers by a hyphen (-).

![Amount in fiat](./assets/images/buy-monto.jpg)

The wizard will ask you the amount, in satoshis, you want to receive. Here you can to use the "Market price" button. If you do so, the rate of [Yadio.io](https://yadio.io/) will be applied.

![Amount in satoshis](./assets/images/buy-price.jpg)

The next thing the wizard prompts you for is the percentage premium or discount you want on your exchange. If you want to increase the market rate (premium), select a positive number; if you want to decrease it (discount), select a negative number. If you want neither, use the "No premium or discount" button.

![Premium or discount](./assets/images/buy-prima.jpg)

Next, you will need to specify the payment method. In this field, you can get creative and add emoticons or whatever you consider to make your offer attractive.

![Payment method](./assets/images/buy-payment-method.jpg)

The bot will proceed to publish your offer in the general or community channel you have set as default. It will remain visible for 23 hours if no one takes it before that time.

![Offer published](./assets/images/buy-public.jpg)

At any time you can cancel the offer, as long as no one has taken it, using the command `/cancel` followed by the order identifier. You can also copy the command plus the identifier into the chat with the bot.

![Cancel order](./assets/images/buy-cancel-order.jpg)

The wizard will return a message confirming the cancellation and your offer will be removed from the offers channel.

![Order cancelled](./assets/images/buy-cancel.jpg)

In case your offer is taken, the wizard will ask you to submit an invoice to Lightning Network with the corresponding amount in satoshis. At the same time, it will ask your counterparty to pay the invoice. 

At this point, the bot will contact both parties to discuss the details of the exchange.

Once you have made the fiat payment, notify the bot with the `/fiatsent` command. The bot will notify your counterpart to check and verify receipt of the money, and proceed to release the satoshis. Remember that your wallet must be online to receive the satoshis.

The exchange is finished. Now you can rate your counterparty.

You can exit the wizard at any time by executing the `/exit` command.

To execute the same purchase order, without using the wizard, you must write your order with the details: `/buy`<amount in sats> <amount in fiat> <fiat code> <payment method> [premium/discount] (without the special characters).

Example: `/buy 100000 50 USD "xyz bank"`.

I buy one hundred thousand sats at fifty dollars payment by xyz bank.

Some examples of purchase orders would be as follows:

- Ex. `/buy 0 50 ves "xyz bank"`: I buy fifty bolivars in sats -in this case, the bot will calculate at the market rate- payment by xyz bank.
- Ex. `/buy 0 10-100 pen "mobile payment"`: I buy from 10 to 100 nuevos soles -in this case, the seller will choose what amount to sell you in that range- payment by mobile payment.
- Ex. `/buy 0 100 eur -3 "mobile payment"`: I buy 100 euros discounting 3% -in this case, the bot will calculate at the market rate discounting or increasing the percentage you choose- payment by mobile payment.

If there is any unsupported variable, the bot will indicate it to you during the order creation process. Once completed, the order will be automatically published in the exchange channel and will be visible for 23 hours.
