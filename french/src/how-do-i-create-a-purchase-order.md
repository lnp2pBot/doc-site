# Comment créer une offre d'achat ?

La procédure est la même que pour l'offre de vente. Seulement, lorsque vous appuyez sur le bouton "Menu", vous devez sélectionner la commande `/buy` au lieu de `/sell`. Cela activera l'assistant qui vous guidera tout au long du processus d'achat.

Une fois activé, l'assistant vous demandera de spécifier la monnaie fiat avec laquelle vous voulez négocier :

![fiat currency](./assets/images/buy-fiat.jpg)

Ensuite, vous devez saisir le montant, en monnaie fiat, que vous souhaitez acheter. N'oubliez pas de ne saisir que des chiffres à cette étape, afin que l'assistant puisse vous comprendre.

Vous pouvez également saisir une fourchette de montants à acheter, en séparant les chiffres par un trait d'union (-).

![Amount in fiat](./assets/images/buy-monto.jpg)

L'assistant vous demandera le montant, en satoshis, que vous souhaitez recevoir. Vous pouvez utiliser le bouton "Prix du marché". Dans ce cas, c'est le tarif de [Yadio.io](https://yadio.io/) qui sera appliqué.

![Amount in satoshis](./assets/images/buy-price.jpg)

L'assistant vous invite ensuite à indiquer le pourcentage de surcote ou de décote que vous souhaitez appliquer à votre échange. Si vous souhaitez vendre au dessus du taux de marché (surcote), sélectionnez un nombre positif ; si vous souhaitez vendre en dessous du taux de marché (décote), sélectionnez un nombre négatif. Si vous ne voulez ni l'un ni l'autre, utilisez le bouton "Pas de surcote ou de décote".

![Premium or discount](./assets/images/buy-prima.jpg)

Ensuite, vous devez spécifier le mode de paiement. Dans ce champ, vous pouvez faire preuve de créativité et ajouter des émoticônes ou tout autre élément que vous jugez susceptible de rendre votre offre attrayante.

![Payment method](./assets/images/buy-payment-method.jpg)

Le bot publiera votre offre dans le canal général ou communautaire que vous avez défini par défaut. Elle restera visible pendant 23 heures si personne ne l'accepte avant ce délai.

![Offer published](./assets/images/buy-public.jpg)

Vous pouvez à tout moment annuler l'offre, tant que personne ne l'a acceptée, en utilisant la commande `/cancel` suivie de l'ID de l'offre. Vous pouvez également copier la commande et l'identifiant dans le chat avec le bot.

![Cancel order](./assets/images/buy-cancel-order.jpg)

L'assistant retournera un message confirmant l'annulation et votre offre sera supprimée du canal des offres.

![Order cancelled](./assets/images/buy-cancel.jpg)

Si votre offre est acceptée, l'assistant vous demandera de soumettre une facture à Lightning Network avec le montant correspondant en satoshis. Dans le même temps, il demandera à votre contrepartie de payer la facture. 

À ce stade, le bot contactera les deux parties pour discuter des détails de l'échange.

Une fois que vous avez effectué le paiement en fiats, informez le robot avec la commande `/fiatsent`. Le bot notifiera à votre contrepartie de vérifier la réception de l'argent, et procédera à la libération des satoshis. Rappelez-vous que votre portefeuille doit être en ligne pour recevoir les satoshis.

L'échange est terminé. Vous pouvez maintenant évaluer votre contrepartie.

Vous pouvez quitter l'assistant à tout moment en exécutant la commande `/exit`.

Pour exécuter la même offre d'achat, sans utiliser l'assistant, vous devez écrire votre commande avec les détails : `/achat`<montant en sats> <montant en fiat> <code fiat> <mode de paiement> [surcote/ décote] (sans les caractères spéciaux).

Exemple : `/buy 100000 20000 XOF "Société Géniale Bank"`.

J'achète 100.000 sats à 20.000 F, payés avec la banque Société Géniale Bank.

Voici quelques exemples d'offres d'achat :

- Ex. `/buy 0 20000 "Société Géniale Bank"` : J'achète pour 20.000 F en sats - dans ce cas, le robot calculera au taux du marché - paiement via la banque Société Géniale Bank.
- Ex. `/buy 0 1000-20000 "Mobile Money"` : J'achète de 1.000 F à 20.000 F en sats - dans ce cas, le vendeur choisira le montant à vous vendre dans cette fourchette - par paiement mobile.
- Ex. `/buy 0 5000000 XOF "Cash RDV Prima Mall 16h UTC" +3` : J'achète 5.000.000 F avec une surcôte (premium) de 3 % - dans ce cas, le robot calculera au taux du marché en décotant le pourcentage que vous avez choisi - par paiement en cash sur rendez-vous au centre commercial Prima à 16h.

S'il existe une variable non prise en charge, le bot vous l'indiquera au cours du processus de création de l'offre. Une fois terminé, l'offre sera automatiquement publiée sur le canal d'échange et sera visible pendant 23 heures.
