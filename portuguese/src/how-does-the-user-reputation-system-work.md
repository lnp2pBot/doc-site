# Como funciona o sistema de reputação do usuário?

A cada transação que você realizar, será solicitado que avalie sua contraparte, ao mesmo tempo em que ela avaliará você. Para isso, o [**lnp2pBot**](https://t.me/lnp2pBot) possui um sistema de classificação de 5 estrelas que permitirá que você avalie sua experiência, onde 1 estrela é a classificação mais baixa e 5 estrelas é a classificação mais alta.

Para obter a reputação, o bot realiza um cálculo iterativo da média e do desvio padrão das avaliações e das transações bem-sucedidas. Portanto, nas primeiras operações, mesmo que você tenha sido avaliado com a pontuação máxima, sua reputação não será alta, mas aumentará progressivamente à medida que você realizar operações com boas avaliações.

Você pode ver esse cálculo em: [https://github.com/lnp2pBot/bot/blob/main/bot/commands.js#L279](https://github.com/lnp2pBot/bot/blob/main/bot/commands.js#L279)

E ele é baseado em:
[https://math.stackexchange.com/questions/2148877/iterative-calculation-of-mean-and-standard-deviation](https://math.stackexchange.com/questions/2148877/iterative-calculation-of-mean-and-standard-deviation)

Quando você cria uma oferta, ela incluirá por padrão o número de transações bem-sucedidas que você realizou, as avaliações recebidas de suas contrapartes e o número de operações feitas. Recomendamos levar todos esses aspectos em consideração ao aceitar uma oferta para evitar golpes.

![Sistema de Reputação](./assets/images/reputation-system.jpg)
