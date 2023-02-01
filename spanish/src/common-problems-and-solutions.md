# Problemas Comunes y sus soluciones

## Intenté pagar una factura con una cartera con fondos insuficientes y [@lnp2pbot](https://t.me/lnp2pbot) ahora me dice que la factura fue usada

Espera 15 minutos a que el tiempo de la transacción expire y la vuelves a iniciar para que se genere una nueva factura.

## Mi contraparte tuvo un problema al enviarme el pago en fiat y luego desapareció, mis sats quedaron bloqueados

La transacción se cancelará automáticamente luego de 23 horas y tus satoshis aparecerán en tu cartera como un pago fallido.

## Un usuario tomó mi compra por error y ya hice el pago en satoshis

Se puede iniciar una cancelacion colectiva. Ambos deben ejecutar el comando `/cancel  <identificador de orden>`

## Cancelé una orden pero los sats no han vuelto a mi wallet, ¿Cuánto debo esperar?

Cuando una orden es cancelada los sats del vendedor retornan inmediátamente al nodo/wallet que realizó el pago. Si utilizas una wallet de auto-custodia o tu propio nodo no tendrás ningún problema pero si utilizas una wallet que custodia tus fondos debes esperar que ellos reflejen tu balance en su sistema interno, esto puede tardar desde unos minutos hasta un par de horas dependiendo de la wallet pero en todas las wallets retorna el 100% de tus fondos, paciencia.
