# Como publicar ofertas em uma comunidade?

Quando você começa a usar o [@lnp2pBot](https://t.me/lnp2pbot), as ordens que você cria são publicadas por padrão em [https://t.me/p2plightning](https://t.me/p2plightning), que é o canal geral onde você pode encontrar ofertas em várias moedas fiat.

Se deseja publicar ofertas em um canal específico para a sua moeda, precisa fazer isso por meio de alguma [comunidade](./communities.md) que a inclua.

- Você pode buscar todas as comunidades que operam com a moeda desejada em [https://market.lnp2pbot.com](https://market.lnp2pbot.com).

- Também pode digitar no bot:

`/findcomms <código da moeda>`

Por exemplo, `/findcomms usd` é usado para buscar todas as comunidades que negociam com USD. Se não souber o código da sua moeda, digite no bot `/listcurrencies` para encontrá-lo.

![Find Community Capture](./assets/images/findcomms.jpg)

Ao selecionar alguma comunidade, o bot mostrará a quantidade de pedidos bem-sucedidos, o volume de negociação operado nas últimas 24 horas e a quantidade de usuários que publicam suas ofertas lá. Para configurar em qual comunidade deseja publicar suas ofertas, deve selecionar o botão "Usar como padrão".

![Community details Capture](./assets/images/comm-detail.jpg)

- Outra maneira de fazer isso é digitando: `/setcomm <@communityGroupName | telegram-group-id>` (`/setcomm` seguido pelo nome do grupo ou seu ID no Telegram).

Para criar uma ordem dentro de uma comunidade, use o comando `/buy` ou `/sell`, dependendo do que deseja. A partir daí, o bot dará as instruções passo a passo e sua oferta será publicada na comunidade selecionada.

![Community Wizard Capture](./assets/images/sell.jpg)

## Mais informações:
- Você só pode ter uma comunidade configurada por padrão de cada vez, portanto, todas as suas ofertas serão publicadas lá.

- Para sair de uma comunidade e voltar a publicar ofertas no [canal geral](https://t.me/p2plightning), deve digitar:
`/setcomm off`

- Se desejar publicar uma oferta em várias comunidades ao mesmo tempo, deve criá-la em cada uma separadamente: primeiro publica em uma, depois configura outra como padrão e publica lá também, e assim por diante para todas as que deseja colocar.

Outra maneira é digitar sua ordem como um comando dentro do chat de uma comunidade que tenha o bot como administrador, pois ele a reconhecerá e publicará a oferta naquela comunidade sem que precise configurá-la como padrão.

- Pode aceitar ofertas de todas as comunidades que desejar sem precisar configurar nenhuma como padrão.
