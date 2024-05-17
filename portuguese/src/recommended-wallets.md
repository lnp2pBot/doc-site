# Carteiras Recomendadas

As seguintes carteiras demonstraram melhor desempenho ao serem usadas com [@lnp2pBot](https://t.me/lnp2pBot):

- [Breez Wallet](https://breez.technology/)
- [Blixt Wallet](https://blixtwallet.github.io/)
- [Phoenix Wallet](https://phoenix.acinq.co/)

#### Observações sobre outras carteiras
- Antes de vender Sats usando qualquer carteira da Lightning Network (ou exchange), informe-se se suporta o pagamento de hold invoices (o tipo de fatura que o bot utiliza como garantia).

- Com a `Wallet of Satoshi`, você pode receber os Sats de uma compra sem nenhum problema, no entanto, se estiver vendendo Sats e a ordem for cancelada, o saldo da sua carteira pode demorar a ser atualizado e os Sats podem não ficar disponíveis até algumas horas depois, mesmo que permaneçam no nó da WoS, devido à atualização do saldo dos usuários em intervalos regulares. Isso pode ocorrer em qualquer outro serviço de custódia, tanto carteiras quanto exchanges que permitam saques na Lightning Network.

- É comum que os pagamentos do [@lnp2pBot](https://t.me/lnp2pBot) para a `Muun wallet` falhem, pois o bot pode pagar uma taxa de roteamento de até 0,2% no máximo. Assim, o pagamento pode falhar se a Muun estiver cobrando taxas maiores do que essa. Nestes casos, é necessário gerar uma nova fatura a partir de outra carteira (Mais informações [aqui](./i-cant-receive.md)). 
Também pode acontecer, ao vender Satoshis da Muun wallet, que a ordem seja cancelada, contudo, mesmo assim, será cobrada uma taxa. Isso ocorre porque a Muun wallet não é uma carteira LN nativa, mas sim uma carteira on-chain que funciona por meio de "submarine swaps". Para realizar uma transação, é necessário pagar a taxa de mineração, mesmo que a fatura do bot tenha sido cancelada.

- Na `Aqua Wallet`, você pode receber os Sats de uma compra sem nenhum problema, mas apesar de ser uma carteira de auto custódia, se estiver vendendo Sats e a ordem for cancelada, o saldo da sua carteira pode demorar várias horas (às vezes até 48 horas) para ser atualizado porque eles têm esse período de espera habilitado para o reembolso de qualquer pagamento que falhe.
