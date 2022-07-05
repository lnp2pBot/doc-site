# ¿Cómo creo una orden de compra?

Al conversar con `@lnp2pbot` encontrarás un botón de menú que te indicará, entre otros, el comando de compra:
`/buy`
Para crearla, debes escribir los detalles de tu orden luego del comando:
`/buy`<monto en sats> <monto en fiat> <código fiat> <método de pago> [prima/descuento] sin los carácteres especiales.

Ejemplo: `/buy 100000 50 usd "xyz bank"`

Compro cien mil sats a cincuenta dólares pago por banco xyz
Algunos ejemplos de órdenes de compra serían los siguientes:

Ej. `/buy 0 50 ves "banco xyz"`: Compro cincuenta bolívares en sats -en este caso el bot hará el cálculo a la tasa de mercado- pago por banco xyz
Ej. `/buy 0 10-100 pen "pago móvil"`: Compro de 10 a 100 nuevos soles -en este caso el vendedor elegirá qué monto venderte en ese rango- pago por pago móvil
Ej. `/buy 0 100 eur -3 "pago móvil"`: Compro 100 euros descontando 3% -en este caso el bot hará el cálculo a la tasa de mercado descontando o incrementando el porcentaje que elijas- pago por pago móvil
De haber alguna variable no compatible, el bot te lo indicará durante el proceso de creación de la orden. Al completarla, la misma se publicará automáticamente en el canal de intercambio y será visible por un período de 23 horas.
