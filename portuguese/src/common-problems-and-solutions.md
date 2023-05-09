# Problemas Comuns e suas soluções

## Tentei pagar uma fatura com uma carteira com fundos insuficientes e [@lnp2pbot](https://t.me/lnp2pbot) agora me diz que a fatura foi usada

Aguarde 15 minutos até que o tempo da transação expire e inicie novamente para gerar uma nova fatura.

## Minha contraparte teve um problema ao me enviar o pagamento em fiat e depois desapareceu, meus satoshis ficaram bloqueados

A transação será cancelada automaticamente após 23 horas e seus satoshis aparecerão em sua carteira como um pagamento cancelado.

## Um usuário tomou minha compra por engano e já fiz o pagamento em satoshis

Pode-se iniciar um cancelamento coletivo. Ambos devem executar o comando `/cancel <identificador de ordem>`

## Cancelei um pedido, mas os sats ainda não voltaram para minha carteira, quanto tempo devo esperar?

Quando um pedido é cancelado, os sats do vendedor são imediatamente devolvidos ao nó/carteira que realizou o pagamento. Se você usa uma carteira de auto-custódia ou seu próprio nó, não terá nenhum problema, mas se usa uma carteira que custodia seus fundos, deve esperar que eles reflitam seu saldo em seu sistema interno, isso pode levar de alguns minutos a algumas horas dependendo da carteira, mas em todas as carteiras, 100% de seus fundos são devolvidos, tenha paciência.
