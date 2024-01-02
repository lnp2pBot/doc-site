# How does the user reputation system work?

For every transaction you conduct, you'll be asked to rate your counterpart, and they'll rate you in return. [**lnp2pBot**](https://t.me/lnp2pBot) uses a 5-star rating system that allows you to evaluate your experience, where 1 star is the lowest rating and 5 stars are the highest.

To determine reputation, the bot conducts an iterative calculation of the mean and standard deviation of the ratings and successful operations. Hence, in the initial transactions, even if you've been rated with the maximum, your reputation won't be high initially. It gradually increases as you conduct more operations with good ratings.

You can see this calculation at: [https://github.com/lnp2pBot/bot/blob/main/bot/commands.js#L279](https://github.com/lnp2pBot/bot/blob/main/bot/commands.js#L279)

It's based on:
[https://math.stackexchange.com/questions/2148877/iterative-calculation-of-mean-and-standard-deviation](https://math.stackexchange.com/questions/2148877/iterative-calculation-of-mean-and-standard-deviation)

When you create an offer, it will include by default the number of successful operations you've conducted, the ratings received from your counterparts, and the number of operations performed. We recommend considering all these aspects when accepting an offer to avoid scams.

![Reputation System](./assets/images/reputation-system.jpg)
