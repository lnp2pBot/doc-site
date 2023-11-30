# Wallets recomendadas

Las siguientes wallets son las que han demostrado un mejor rendimiento al usarlas con [@lnp2pBot](https://t.me/lnp2pBot)

- [Breez Wallet](https://breez.technology/)
- [Blixt Wallet](https://blixtwallet.github.io/)
- [Phoenix Wallet](https://phoenix.acinq.co/)
- [@LightningTipBot](https://t.me/LightningTipBot)

#### Notas sobre otras wallets
Con `Wallet of Satoshi`, o cualquier otro servicio custodial, puede pasar que si estás vendiendo Sats y se cancela la orden, demore en actualizarse el balance de tu wallet y no aparezcan disponibles los Sats hasta pasadas algunas horas, aunque estén en el nodo de la wallet, eso se debe a que las wallets custodials actualizan el saldo de sus usuarios cada cierto tiempo, por lo que deberás esperar unas horas.

Es común que los pagos de [@lnp2pBot](https://t.me/lnp2pBot) hacia `Muun wallet` fallen porque el bot puede pagar un fee de ruteo de hasta 0.2% máximo, así que no podrá pagar la factura cuando Muun esté cobrando fees mayores a ese, en dichos casos se debe poner una nueva invoice desde otra wallet (Más info [aquí](./i-cant-receive.md)). 
También puede pasar que estés vendiendo Sats desde Muun wallet y se cancele la orden, de todas formas cobrará un fee porque Muun wallet no es una wallet LN nativa, sino onchain que funciona mediante submarine swaps, y para hacer una transacción debes pagar el fee de minería aunque la hold invoice del bot haya sido cancelada.  
