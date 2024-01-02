# Problèmes courants et solutions

## J'ai essayé de payer une facture avec un portefeuille ne disposant pas des fonds nécessaires et [@lnp2pbot](https://t.me/lnp2pbot) me dit maintenant que la facture a été utilisée.

Attendez 15 minutes que la durée de la transaction expire et relancez-la pour qu'une nouvelle facture soit générée.

## Ma contrepartie a eu un problème pour m'envoyer le paiement en fiat et ensuite il a disparu, mes sats ont été bloqués.

La transaction sera automatiquement annulée sous 23 heures et vos satoshis apparaîtront dans votre porte-monnaie comme un paiement échoué.

## Un utilisateur a pris mon offre par erreur alors que j'avais déjà effectué le paiement en satoshis.

Une annulation coopérative peut être initiée. L'initiateur doit exécuter la commande `/cancel <ID de l'offre>` et la contrepartie n'a qu'à exécuter `/cancel` et confirmer.

## J'ai annulé une commande mais les sats ne sont pas revenus dans mon portefeuille, combien de temps dois-je attendre ?

Lorsqu'une commande est annulée, les sats du vendeur retournent immédiatement au nœud/portefeuille qui a effectué le paiement. Si vous utilisez un portefeuille à auto-détention (self-custodial) ou bien votre propre nœud, vous n'aurez aucun problème. Si vous utilisez un portefeuille qui héberge vos fonds (custodial), vous devez attendre qu'il reflète votre solde dans son système interne, ce qui peut prendre de quelques minutes à quelques heures selon le portefeuille, mais dans tous les cas, 100 % de vos fonds vous seront rendus, soyez patient.
