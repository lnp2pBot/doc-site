# ¿Cómo creo una orden de compra?

Al conversar con [@lnp2pbot](https://t.me/lnp2pbot) encontrarás un botón de menú que te indicará, entre otros, el comando de compra:
`/buy`, eso activará al ayudante (o wizard) que te guiará por el proceso de comprar .

![Iniciar el asistente](./assets/images/buy-start.jpg)

Una vez activado, te pedirá que especifiques la moneda fiat en la que quieres transar:

![Moneda Fiat](./assets/images/buy-fiat.jpg)

A continuación deberás introducir el monto (en la moneda fiat) que quieres comprar. Recuerda ingresar solo números en este paso, para que el asistente te pueda entender.

También puedes introducir un rango de cantidades a comprar, separando los números por un guión (-).

![Cantidad de fiat](./assets/images/buy-monto.jpg)

El asistente te preguntará el monto, en satoshis, que quieres recibir. Aquí tienes la posibilidad de usar el botón 'Precio del mercado'; si lo haces, se tomará la tasa de [Yadio.io](https://yadio.io/).

![Cantidad en satoshis](./assets/images/buy-price.jpg)

Lo siguiente que te solicita el asistente es la prima o descuento que quieres en tu intercambio. Si quierres añadir, usa un número positvo, si quieres disminuir, usa un número negativo. En caso de no querer ninguna, coloca 0.

![Prima o descuento](./assets/images/buy-prima.jpg)

Deberás especificar el método de pago a continuación, en este campo es donde puedes ponerte creativo y añadir emoticones o lo que consideres para hacer atractiva tu oferta.

![Método de pago](./assets/images/buy-payment-metod.jpg)

El robot procederá a publicar tu oferta en el canal general o el de la comunidad que hayas configurado como predeterminada, permanecerá visible por 23 horas, sí nadie la toma antes de ese tiempo.

![Oferta publicada](./assets/images/buy-public.jpg)

En cualquier momento puedes cancelar la oferta, siempre y cuando nadie la haya tomado, con el comando `Cancel` seguido por el identificador de la orden, o copiando el comando mas el identificador en el chat con el robot

![Cancelar orden](./assets/images/buy-cancel-order.jpg)

Se te devolverá un mensaje confirmando la cancelación y se removerá tu oferta del canal de ofertas

![Orden cancelada](./assets/images/buy-cancel.jpg)

En caso de que tu oferta sea tomada se te pedirá que entregues una factura en Ligthning Network con el monto en satoshis correspondiente, al mismo tiempo se le pedirá a tu contraparte que pague una factura. 

Es en este momento en que el robot pondrá en contacto a ambas partes para que discutan los detalles del intercambio. 

Una vez que hayas hecho el pago en fiat, notifica al robot con el comando `fiatsent` el robot avisará a tu contraparte para que consulte y certifique haber recibido el dinero y proceda a liberar los satoshis. Recuerda que para recibirlos, tu cartera deberá estar en linea.

El intercambio ha terminado, puedes ahora calificar a tu contraparte.


Para ejecutar la misma orden de venta, sin usar el asistente, debes escribir tu orden con los detalles: `/buy`<monto en sats> <monto en fiat> <código fiat> <método de pago> [prima/descuento] sin los carácteres especiales.

Ejemplo: `/buy 100000 50 usd "xyz bank"`

Compro cien mil sats a cincuenta dólares pago por banco xyz
Algunos ejemplos de órdenes de compra serían los siguientes:

- Ej. `/buy 0 50 ves "banco xyz"`: Compro cincuenta bolívares en sats -en este caso el bot hará el cálculo a la tasa de mercado- pago por banco xyz
- Ej. `/buy 0 10-100 pen "pago móvil"`: Compro de 10 a 100 nuevos soles -en este caso el vendedor elegirá qué monto venderte en ese rango- pago por pago móvil
- Ej. `/buy 0 100 eur -3 "pago móvil"`: Compro 100 euros descontando 3% -en este caso el bot hará el cálculo a la tasa de mercado descontando o incrementando el porcentaje que elijas- pago por pago móvil

De haber alguna variable no compatible, el bot te lo indicará durante el proceso de creación de la orden. Al completarla, la misma se publicará automáticamente en el canal de intercambio y será visible por un período de 23 horas.
