# مشکلات رایج و راه‌حل‌ها

### من سعی می‌کنم سفارش بردارم، اما هیچ اتفاقی نمی‌افتد

هنگامی که دکمه «خرید ساتوشی» یا «فروش ساتوشی» یک سفارش را فشار می‌دهید، [@lnp2pbot](https://t.me/lnp2pBot) به صورت خصوصی به شما پیام خواهد داد که در هر مرحله چه کارهای را برای تکمیل سفارش انجام دهید.
برای اینکه ربات به درخواست شما پاسخ دهد، لازم است [با آن شروع به کار کرده باشید](./how-do-i-initialize-the-bot.md) زیرا اگر قبلاً از آن استفاده نکرده باشید، هیچ رباتی نمی‌تواند در ابتدا با شما چت باز کرده و بهتان پیام خصوصی دهد. پس [@lnp2pbot](https://t.me/lnp2pBot) را باز کرده و دستور 'start/' را تایپ کنید یا روی دکمه 'Start' ضربه بزنید، سپس دوباره سفارش را انجام دهید، به ربات برگردید و دستورالعمل‌های آن را دنبال کنید.
- اگر قبلاً از ربات استفاده می‌کردید و آخرین باری که این کار را انجام دادید قبل از مارس 2023 بود، باید آن را با دستور 'start/' مجدداً راه اندازی کنید زیرا ربات ریست شده است و پایگاه داده قبلی آن حفظ نشده.

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
