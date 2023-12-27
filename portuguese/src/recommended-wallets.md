# Carteiras Recomendadas

As seguintes carteiras demonstraram melhor desempenho ao serem usadas com [@lnp2pBot](https://t.me/lnp2pBot):

- [Breez Wallet](https://breez.technology/)
- [Blixt Wallet](https://blixtwallet.github.io/)
- [Phoenix Wallet](https://phoenix.acinq.co/)
- [@LightningTipBot](https://t.me/LightningTipBot)

#### Observações sobre outras carteiras
Com a `Wallet of Satoshi` ou qualquer outro serviço custodial, pode acontecer que, se estiver vendendo Satoshis e a ordem for cancelada, o saldo na sua carteira demore a ser atualizado e os Satoshis não apareçam como disponíveis até algumas horas depois, mesmo que estejam no nó da carteira. Isso ocorre porque as carteiras custodiais atualizam o saldo de seus usuários em intervalos específicos, o que pode demandar algumas horas de espera.

É comum que os pagamentos do [@lnp2pBot](https://t.me/lnp2pBot) para a `Muun wallet` falhem, pois o bot pode pagar uma taxa de roteamento de até 0,2% no máximo. Assim, o pagamento pode falhar se a Muun estiver cobrando taxas maiores do que essa. Nestes casos, é necessário gerar uma nova fatura a partir de outra carteira (Mais informações [aqui](./i-cant-receive.md)). 
Também pode acontecer, ao vender Satoshis da Muun wallet, que a ordem seja cancelada, contudo, mesmo assim, será cobrada uma taxa. Isso ocorre porque a Muun wallet não é uma carteira LN nativa, mas sim uma carteira on-chain que funciona por meio de "submarine swaps". Para realizar uma transação, é necessário pagar a taxa de mineração, mesmo que a fatura do bot tenha sido cancelada.
