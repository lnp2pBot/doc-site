# ¿Cómo sé si el vendedor realmente liberó los sats?

Si @lnp2pBot te dice que el vendedor liberó, es porque realmente es así, pero si quieres verificarlo puedes hacerlo de la siguiente manera:

Escríbele al bot `/listorders` y si el bot aún está en proceso de pagar tu factura el status que verás será `PAID_HOLD_INVOICE`, si el bot ya pagó la factura la orden no aparecerá en la lista.

Cuando una orden tiene status `PAID_HOLD_INVOICE`, el vendedor ya no tiene ninguna responsabilidad debido a que ha liberado los sats, si tienes problemas para recibir ve a la sección [El vendedor liberó pero no me llegan los sats a mi wallet](./i-cant-receive.md).
