# Comment puis-je savoir si le vendeur a réellement libéré les sats ?

Si @lnp2pBot vous dit que le vendeur a libéré les sats, c'est vraiment le cas, mais si vous voulez le vérifier, vous pouvez le faire de la manière suivante :

Ecrivez au bot `/listorders` et si le bot est encore en train de régler votre facture, le statut que vous verrez sera `PAID_HOLD_INVOICE`, si le bot a déjà réglé la facture, la commande n'apparaîtra pas sur la liste.

Lorsqu'une offre a le statut `PAID_HOLD_INVOICE`, le vendeur n'a plus aucune responsabilité car il a libéré les sats, si vous avez des problèmes de réception, allez à la section [Le vendeur a libéré mais je ne reçois pas les sats dans mon porte-monnaie](./i-cant-receive.md).