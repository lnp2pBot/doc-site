# How do I post offers in a community?

When you start using [@lnp2pBot](https://t.me/lnp2pbot), the orders you create are by default posted in [https://t.me/p2plightning](https://t.me/p2plightning), which is the general channel where you can find offers in various fiat currencies.

If you want to post offers in a channel specifically for your currency, you need to do so through a [community](./communities.md) that incorporates it.

- You can search for all communities operating with the desired currency at [https://market.lnp2pbot.com](https://market.lnp2pbot.com).

- You can also type within the bot:

`/findcomms <fiat code>`

For example, `/findcomms usd` is used to search for all communities trading with USD. If you don't know your currency code, type `/listcurrencies` in the bot and find it.

![Find Community Capture](./assets/images/findcomms.jpg)

Upon selecting a community, the bot will display the number of successful orders, the trading volume operated in the last 24 hours, and the number of users posting their offers there. To set which community you want to publish your offers in, you should select the "Use as default" button.

![Community details Capture](./assets/images/comm-detail.jpg)

- Another way to do it is by typing:
`/setcomm <@communityGroupName | telegram-group-id>` (`/setcomm` along with the group name or its Telegram ID).

To create an order within a community, use the `/buy` or `/sell` command depending on what you want. From there, the bot will give you step-by-step instructions, and your offer will be published in the selected community.

![Community Wizard Capture](./assets/images/sell.jpg)

## More Information:
- You can only have one community configured by default at a time, and therefore, all your offers will be posted there.

- To leave a community and post offers again in the [general channel](https://t.me/p2plightning), you should type:
`/setcomm off`

- If you want to post an offer in multiple communities simultaneously, you need to create it in each one separately: first, post it in one, then configure another as default and post there as well, and so on for all the communities you want it in.

Another way is to type your order as a command within the chat of a community where the bot is an administrator, as it will recognize it and post the offer in that community without you needing to set it as default.

- You can take offers from as many communities as you want without having to configure any of them as default.
