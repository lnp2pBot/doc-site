# O vendedor liberou, mas os Sats não chegaram à minha carteira
## Possíveis causas
Às vezes, o bot não encontra rotas bem-sucedidas para o pagamento por várias razões, às vezes simplesmente porque não há uma boa conexão do remetente ao destinatário, mas outras vezes é muito mais complicado, pode ser que os nós conectados ao destinatário estejam cobrando taxas muito altas.

O nó do [@lnp2pBot](https://t.me/lnp2pBot) está disposto a pagar até 0.2% do valor total da operação em taxas de roteamento. Se essa taxa for maior, o bot simplesmente não fará o pagamento. Algumas carteiras que não são nativas da Lightning podem cobrar mais de 0.2% quando a mempool está congestionada; para essas carteiras, o bot não conseguirá pagar (mais informações sobre carteiras [aqui](./recommended-wallets.md)).

Outro caso é se você não tiver `inbound capacity`, por exemplo, se estiver usando a carteira Blixt e tiver um canal recém-aberto nela, todo o dinheiro nessa carteira será de saída e você não terá capacidade para receber. Nesse caso, todos os pagamentos para essa carteira falharão. Existem carteiras modernas como a Phoenix Wallet que resolvem esse problema informando que você não tem capacidade de entrada e propõem modificar o canal ([splice in](https://bitcoinops.org/en/topics/splicing/)) para que o novo pagamento recebido esteja do lado do usuário (mais capacidade de entrada). Esta carteira cobra uma comissão por isso.

## Solução
Quando um pagamento falha, o bot tentará pagá-lo mais 2 vezes em intervalos de 5 minutos. Se ainda não for possível fazer o pagamento, ele pedirá que você forneça uma nova fatura para continuar tentando. É recomendável que você a gere de outra [carteira](./recommended-wallets.md).

Se você não inserir a fatura antes de 20 minutos após o bot solicitá-la, o assistente será cancelado e o bot não solicitará mais. Nesse caso, você precisará inseri-la com o comando
`/setinvoice <order id> <fatura lightning>` 
(Não escreva os símbolos <>, separe cada parte com um espaço, não reutilize faturas).

Se você tentou várias vezes e ainda não recebeu os Sats, mantenha a calma, pois a operação não pode mais ser cancelada ou os Sats devolvidos ao vendedor, eles estão no nó do bot e você pode continuar tentando com novas faturas quantas vezes forem necessárias até recebê-los.
