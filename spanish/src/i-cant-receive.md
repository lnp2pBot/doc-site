# El vendedor liberó pero no me llegan los sats a mi wallet

En ocasiones el bot no encuentra rutas exitosas para realizar el pago por diferentes razones, a veces porque simplemente no hay una buena conexión del origen al destino pero otras veces es mucho más complicado, puede ocurrir que los nodos conectados al destino cobran fees muy altas, el nodo de @lnp2pBot está dispuesto a pagar hasta un 0.2% del monto total de la operación en routing fee, si este fee es mayor el bot simplemente no realizará el pago, algunas wallets que no son nativas lightning puede que cobren más de 0.2% cuando la mempool está congestionada, a esas wallets el bot no les podrá pagar.

Otro caso es que no tengas `inbound capacity`, te doy un ejemplo, si usas Blixt wallet y en ella tienes un canal que recien abres, todo el dinero en esa wallet sería de salida, no tienes capacidad para recibir, en ese caso todos los pagos hacia esa wallet van a fallar, hay wallets modernas como Phoenix wallet que resuelve este problema indicandote que no tienes inbound capacity y te propone abrirte un nuevo canal, esta wallet cobra una comisión por esto.

Como solución [recomendamos probar diferentes wallets](./recommended-wallets.md), generar nuevas facturas y entregarselas al bot para que intente enviarte el pago nuevamente.
