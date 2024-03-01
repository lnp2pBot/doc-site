# تکمیل یک سفارش

بسیاری از اختلافات به این دلیل به وجود می‌آیند که یکی از طرفین در پاسخ دادن به یک پیام تاخیر دارد، سوء تفاهم یا تاخیر در پرداخت وجود دارد. اینها موارد ساده ای هستند که فقط به اندکی صبر و کمک در برقراری ارتباط نیاز دارند.

موارد دیگر شامل قصد بدخواهانه است، مانند زمانی که فروشنده می‌خواهد پول فیات را نگه دارد و ساتوشی‌ها را هم پس بگیرد. در این موارد، حل کننده می‌تواند دستور '/settleorder/` را اجرا کند که پرداخت دریافتی را شناسایی کرده و به طور خودکار ساتوشی‌ها را برای خریدار ارسال می‌کند. توجه کنید که مدیر در صورت تشخیص چنین اتفاقی میتواند فرد متقلب(چه فروشنده چه خریدار) را، از استفاده مجدد از ربات به طور کلی منع کند.

![Completing an Order](./assets/images/settleorder.png)

## تکمیل سفارش زمانی که رسیدن فیات خیلی طول می‌کشد
در [@lnp2pbot](https://t.me/lnp2pBot)، روش‌های پرداختی که انتقال فوری فیات را تضمین می‌کنند باید استفاده شود. با این حال، ممکن است مواردی وجود داشته باشد که بیشتر از حد معمول طول بکشد تا وجه فیات به فروشنده برسد. برای مثال، به دلیل مشکلاتی در پردازش پرداخت توسط بانک.
در چنین شرایطی، خریدار این احتمال را به خطر می‌اندازد که فروشنده فیات را [قبل از انقضای فاکتور نگهداری](./how-long-does-it-to-finalize-a-transaction.md) دریافت نکند، بنابراین نه رها کردن ساتوشی‌ها با این حال، پس از انقضای آن، فروشنده مجدداً ساتوشی‌ها و به دنبال آن فیات را خواهد داشت. پس از آن خریدار تحت الحمایه حسن نیت فروشنده قرار می‌گیرد که ممکن است ساتوشی ها را بدون دخالت ربات ارسال کند یا ندهد. برای جلوگیری از این امر، کاربران می‌توانند به حل‌کننده‌های کامیونیتی خود مراجعه کنند تا آنها به عنوان واسطه عمل کنند.

A solver can make the bot charge the hold invoice from the seller using the `/freezeorder <order_id>` command. This way, they can wait long enough for the fiat to arrive, and when it does, the solver will release the sats using the `/paytobuyer <order_id>` command. The buyer's invoice may have expired during the process, so they'll need to update it by typing `/setinvoice <order id> <lightning invoice>`.

This solution implies custody of the sats by the bot and should only be used when no other options exist.
