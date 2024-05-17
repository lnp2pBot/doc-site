# Wallets recomendadas

Las siguientes wallets son las que han demostrado un mejor rendimiento al usarlas con [@lnp2pBot](https://t.me/lnp2pBot)

- [Breez Wallet](https://breez.technology/)
- [Blixt Wallet](https://blixtwallet.github.io/)
- [Phoenix Wallet](https://phoenix.acinq.co/)

#### Notas sobre otras wallets
- Antes de vender Sats usando cualquier wallet de Lightning Network (o exchange) infórmate si soporta el pago de hold invoices (el tipo de  invoices que el bot utiliza como scrow).

- Con `Wallet of Satoshi` puedes recibir los Sats de una compra sin ningún problema, sin embargo, si estás vendiendo Sats y se cancela la orden, el balance de tu wallet puede tardar en actualizarse y no aparecer disponibles los Sats hasta pasadas algunas horas, aunque permanezcan en el nodo de WoS, debido a que actualiza el saldo de sus usuarios cada cierto tiempo. Esto puede ocurrir en cualquier otro servicio custodial, tanto wallets como exchanges que tengan habilitados retiros en Lightning Network.

- Es común que los pagos de [@lnp2pBot](https://t.me/lnp2pBot) hacia `Muun wallet` fallen porque el bot puede pagar un fee de ruteo de hasta 0.2% máximo, así que no podrá pagar la factura cuando Muun esté cobrando fees mayores a ese, en dichos casos se debe poner una nueva invoice desde otra wallet (Más info [aquí](./i-cant-receive.md)). 
También puede pasar que estés vendiendo Sats desde Muun wallet y se cancele la orden, de todas formas cobrará un fee porque Muun wallet no es una wallet LN nativa, sino onchain que funciona mediante submarine swaps, y para hacer una transacción debes pagar el fee de minería aunque la hold invoice del bot haya sido cancelada.

- En `Aqua Wallet` puedes recibir los Sats de una compra sin ningún problema, pero a pesar de ser una wallet de auto custodia si estás vendiendo Sats y se cancela la orden, el balance de tu wallet tardará en actualizarse varias horas (en ocasiones hasta 48 horas) porque tienen habilitado ese período de espera para el reembolso de cualquier pago que falle.
