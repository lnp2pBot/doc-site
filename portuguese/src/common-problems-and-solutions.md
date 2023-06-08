# Problemas comuns e suas soluções

## Eu tentei pagar uma fatura com uma carteira sem fundos suficientes e o [@lnp2pbot](https://t.me/lnp2pbot) agora me diz que a fatura foi usada

Aguarde 15 minutos para que o tempo da transação expire e tente novamente para gerar uma nova fatura.

## Minha contraparte teve um problema ao me enviar o pagamento em moeda fiduciária e depois desapareceu, meus sats foram bloqueados

A transação será cancelada automaticamente após 23 horas e seus satoshis aparecerão em sua carteira como um pagamento falhado.

## Um usuário pegou minha compra por engano e eu já fiz o pagamento em satoshis

Uma cancelação cooperativa pode ser iniciada. O iniciador deve executar o comando `/cancel <identificador da ordem>` e a contraparte só precisa executar `/cancel` e tocar no botão para confirmar.

## Cancelei um pedido, mas os sats não voltaram para minha carteira, quanto tempo devo esperar?

Quando um pedido é cancelado, os sats do vendedor retornam imediatamente para o nó/carteira que fez o pagamento. Se você usa uma carteira de custódia própria ou seu próprio nó, não terá problemas, mas se usa uma carteira que custodia seus fundos, você deve esperar que eles sejam refletidos em seu saldo no sistema interno da carteira. Isso pode levar alguns minutos a algumas horas, dependendo da carteira, mas em todas as carteiras ele retorna 100% dos seus fundos. Seja paciente.
