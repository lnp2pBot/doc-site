# Portefeuilles recommandés

Les portefeuilles suivants sont ceux qui ont montré de meilleures performances lorsqu'ils ont été testés avec le [@lnp2pBot](https://t.me/lnp2pBot):

- [Breez Wallet](https://breez.technology/)
- [Blixt Wallet](https://blixtwallet.github.io/)
- [Phoenix Wallet](https://phoenix.acinq.co/)

#### Remarques sur d'autres portefeuilles
- Avant de vendre des Sats en utilisant n'importe quel portefeuille du réseau Lightning (ou une plateforme d'échange), renseignez-vous pour savoir s'il prend en charge le paiement des hold invoices (le type de factures que le bot utilise comme garantie).

- Avec `Wallet of Satoshi`, vous pouvez recevoir les Sats d'un achat sans aucun problème. Cependant, si vous vendez des Sats et que la commande est annulée, le solde de votre portefeuille peut mettre du temps à se mettre à jour et les Sats peuvent ne pas être disponibles pendant plusieurs heures, même s'ils restent sur le nœud de WoS, car il met à jour le solde de ses utilisateurs à intervalles réguliers. Cela peut se produire avec tout autre service de garde, que ce soit des portefeuilles ou des plateformes d'échange autorisant les retraits sur le réseau Lightning.

- Il est courant que les paiements de [@lnp2pBot](https://t.me/lnp2pBot) vers le portefeuille `Muun` échouent car le bot peut payer des frais de routage allant jusqu'à 0,2 % au maximum. Ainsi, il ne pourra pas payer la facture lorsque Muun facture des frais supérieurs à cela. Dans de tels cas, vous devez générer une nouvelle facture depuis un autre portefeuille (Plus d'informations [ici](./i-cant-receive.md)). Il peut également arriver que vous vendiez des Sats depuis le portefeuille Muun et que la commande soit annulée. Dans tous les cas, des frais seront facturés car le portefeuille Muun n'est pas un portefeuille natif du réseau Lightning, mais fonctionne via des swaps sous-marins, et pour effectuer une transaction, vous devez payer les frais miniers même si la facture en attente du bot a été annulée.

- Dans `Aqua Wallet`, vous pouvez recevoir les Sats d'un achat sans aucun problème, mais malgré le fait qu'il s'agisse d'un portefeuille à auto-custody, si vous vendez des Sats et que la commande est annulée, le solde de votre portefeuille mettra du temps à se mettre à jour, parfois jusqu'à 48 heures, car ils ont activé cette période d'attente pour le remboursement de tout paiement échoué.
