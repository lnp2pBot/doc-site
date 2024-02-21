# What exchange rate does the bot use?

When creating an order, you can choose to specify only the fiat amount to `pay/receive`, without indicating the quantity of sats you want to `buy/sell`. In this case, you should select the `Market Price` button, and the bot will calculate the market rate offered by [yadio.io](https://yadio.io/) at the moment your order is taken.

![Market Price](./assets/images/market-price.gif)

When you select the `Market Price` button, you can also set a premium or discount for your offer. This means an increase or decrease will be applied to the bitcoin price indicated by [yadio.io](https://yadio.io/) at the time the offer is taken.

#### Practical examples with their meanings:

- Buying Sats +1%: I want to buy Sats 1% more expensive (above) than the BTC price indicated by [yadio.io](https://yadio.io/) at the time someone takes my offer.

- Buying Sats -5%: I want to buy Sats 5% cheaper (below) than the BTC price indicated by [yadio.io](https://yadio.io/) at the time someone takes my offer.

- Selling Sats +3%: I want to sell Sats 3% more expensive (above) than the BTC price indicated by [yadio.io](https://yadio.io/) at the time someone takes my offer.

- Selling Sats -4%: I want to sell Sats 4% cheaper (below) than the BTC price indicated by [yadio.io](https://yadio.io/) at the time someone takes my offer.
