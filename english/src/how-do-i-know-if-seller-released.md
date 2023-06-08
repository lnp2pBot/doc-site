# How do I know if the seller actually released the sats?

If @lnp2pBot tells you that the vendor released, it really is, but if you want to verify it you can do it as follows:

Write to the bot `/listorders` and if the bot is still in the process of paying your invoice the status you will see will be `PAID_HOLD_INVOICE`, if the bot has already paid the invoice the order will not appear on the list.

When an order has status `PAID_HOLD_INVOICE`, the seller no longer has any responsibility because he/she has released the sats, if you have problems receiving go to the section [The seller released but I don't get the sats in my wallet](./i-cant-receive.md).
