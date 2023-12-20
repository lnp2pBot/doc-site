# Completando una orden

Muchas disputas se inician porque una de las dos partes tardó en responder un mensaje, hubo un malentendido o una demora en algún pago. Estos son casos sencillos que solo requieren paciencia y ayudar en la comuncación.
Otros casos involucran malicia, como por ejemplo puede haber un vendedor que quiera quedarse con el dinero fiat y que le retornen los sats. Para estos casos el solver puede ejecutar el comando `/settleorder`, lo que hace este comando es que reconoce el pago recibido y automáticamente envía los sats al comprador.

![Completando una orden](./assets/images/settleorder.png)

## Completando una orden cuando el fíat tarda demasiado en llegar
Con [@lnp2pbot](https://t.me/lnp2pBot) se deben utilizar métodos de pago que garanticen que el envío del fíat sea instantáneo. Sin embargo, puede haber casos en los que el fíat demore más de lo habitual en llegar al vendedor de Sats, por ejemplo, debido a problemas en el procesamiento del pago por parte del banco. 
En tales situaciones, el comprador corre el riesgo de que el vendedor no reciba el fíat [antes de que caduque la hold invoice](./how-long-does-it-take-to-finalize-a-transaction.md) y por tanto no libere los Sats, pero cuando caduque, el vendedor tendrá los Sats de nuevo, y luego el fíat. El comprador quedaría a expensas de la buena voluntad del vendedor que podría enviarle los satoshis o no, sin que el bot pueda tener ninguna intervención en esto. Para evitarlo, los usuarios pueden acudir a los solvers de su comunidad que actuarán como mediadores. 

Un solver puede hacer que el bot cobre la hold invoice del vendedor utilizando el comando `/freezeorder <order_id>`,
así podrían esperar el tiempo suficiente para que el fíat llegue, y cuando ocurra, el solver liberará los Sats con el comando `/paytobuyer <order_id>`. Es posible que la factura del comprador haya expirado durante el proceso, por lo que deberá actualizarla escribiendo `/setinvoice <order id> <lightning invoice>`.

Esta solución implica la custodia de los Sats por parte del bot y debe utilizarse solo cuando no existan otras opciones.
