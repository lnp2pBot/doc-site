# Problemas Comunes y sus soluciones

### Estoy intentando tomar una orden y no pasa nada 

Al pulsar el botón `Comprar satoshis` o `Vender satoshis` de una oferta, [@lnp2pbot](https://t.me/lnp2pBot) te responderá por privado lo que debes hacer para completar el proceso. 
Para que el bot pueda responder a tu solicitud es necesario que lo [inicialices](./how-do-i-initialize-the-bot.md), pues ningún bot puede abrirte un chat de primero si no lo has usado antes. Abre [@lnp2pbot](https://t.me/lnp2pBot) y escribe el comando `/start` o toca el botón de `Iniciar`, luego intenta nuevamente tomar la orden, regresa al bot y sigue sus instrucciones.
- Si ya usabas el bot y la última vez que lo hiciste fue antes de marzo de 2023, debes volver a inicializarlo con el comando `/start` porque fue reiniciado y no se conservó su base de datos anterior.

### Intenté pagar una factura con una cartera con fondos insuficientes y [@lnp2pbot](https://t.me/lnp2pbot) ahora me dice que la factura fue usada

Espera 15 minutos a que el tiempo de la transacción expire y vuélvela a iniciar para que se genere una nueva factura.

### Mi contraparte tuvo un problema al enviarme el pago en fíat y luego desapareció, mis sats quedaron bloqueados

La transacción se cancelará automáticamente luego de 23 horas y tus satoshis aparecerán en tu cartera como un pago fallido. Si quieres acelerar el proceso puedes abrir una disputa con el comando `/dispute <order id>`.

### Un usuario tomó mi compra por error y ya hice el pago en satoshis

Se puede iniciar una cancelación cooperativa. Ambos deben ejecutar el comando `/cancel <order id>`.

### Cancelé una orden pero los sats no han vuelto a mi wallet. ¿Cuánto debo esperar?

Cuando una orden es cancelada los sats del vendedor retornan inmediatamente al nodo/wallet que realizó el pago. Si utilizas una wallet de auto-custodia o tu propio nodo no tendrás ningún problema, pero si utilizas una wallet que custodia tus fondos debes esperar que ellos reflejen tu balance en su sistema interno, esto puede tardar desde unos minutos hasta un par de horas dependiendo de la wallet, pero en todas las wallets retorna el 100% de tus fondos, paciencia.

### Estoy comprando y el bot no me pide una invoice, sino que me pone directamente en contacto con el vendedor

Esto pasa cuando tienes activada una lightning address. En ese caso los Sats que compres serán enviados directamente hacia allí sin pedirte una nueva invoice en cada compra. Para revisar tu lightning address escribe dentro del [bot](https://t.me/lnp2pbot) el comando `/settings`, si quieres desactivarla escribe dentro del [bot](https://t.me/lnp2pbot) el comando  `/setaddress off`.
