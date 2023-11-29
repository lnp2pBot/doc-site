# El vendedor liberó pero no me llegan los Sats a mi wallet
## Posibles causas
En ocasiones el bot no encuentra rutas exitosas para realizar el pago por diferentes razones, a veces porque simplemente no hay una buena conexión del origen al destino pero otras veces es mucho más complicado, puede ocurrir que los nodos conectados al destino cobren fees muy altas.

El nodo de [@lnp2pBot](https://t.me/lnp2pBot) está dispuesto a pagar hasta un 0.2% del monto total de la operación en routing fee, si este fee es mayor el bot simplemente no realizará el pago, algunas wallets que no son nativas lightning puede que cobren más de 0.2% cuando la mempool está congestionada, a esas wallets el bot no les podrá pagar (más información sobre wallets [aquí](./recommended-wallets.md)).

Otro caso es que no tengas `inbound capacity`, por ejemplo, si usas Blixt wallet y en ella tienes un canal que recién abres, todo el dinero en esa wallet sería de salida y no tendrías capacidad para recibir, en ese caso todos los pagos hacia esa wallet van a fallar. Hay wallets modernas como Phoenix wallet que resuelven este problema indicándote que no tienes inbound capacity y propone modificar el canal ([splice in](https://bitcoinops.org/en/topics/splicing/)) para que el nuevo pago recibido esté del lado del usuario (más inbound capacity), esta wallet cobra una comisión por esto.

## Solución
Cuando un pago falla el bot intentará pagarlo 2 veces más en intervalos de 5 minutos, si continúa sin poder hacerlo te pedirá que le entregues una nueva factura para seguir intentándolo, es recomendable que la generes desde otra [wallet](./recommended-wallets.md). 

Si no introduces la factura antes de 20 minutos después que el bot la pida, se cancelará ese asistente y no la seguirá pidiendo luego. En ese caso deberás ponerla con el comando
`/setinvoice <order id> <lightning invoice>` 
(No debes escribir los símbolos <>, separa cada parte con un espacio, no reutilices facturas).

Si llevas varios intentos y aún no recibes los Sats, mantén la calma, pues ya no es posible que se cancele la operación o le sean devueltos los Sats al vendedor, sino que están en el nodo del bot y puedes seguir intentando con nuevas invoices las veces que sean necesarias hasta que los recibas.
