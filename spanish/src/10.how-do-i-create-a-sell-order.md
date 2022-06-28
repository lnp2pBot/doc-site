#  ¿Cómo creo una orden de venta?

El procedimiento es exactamente el mismo a la orden de compra, sustituyendo el comando  `/buy` por `/sell`

Debes escribir tu orden con los detalles: ` /sell <monto en sats> <monto en fiat> <código fiat> <método de pago> [prima/descuento]`  sin los carácteres especiales.

Ej. /`sell 100000 50 usd "banco xyz"` Vendo cien mil sats a cincuenta dólares cobro por banco xyz
Tal como en las órdenes de venta, en caso de haber alguna variable no compatible el bot te lo indicará durante el proceso de creación de la orden. Al completarla, la misma se publicará en el canal de intercambio y será visible por un período de 23 horas.
