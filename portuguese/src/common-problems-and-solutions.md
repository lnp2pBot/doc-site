# Problemas Comuns e Suas Soluções

### Estou tentando aceitar um pedido e nada acontece

Ao pressionar o botão 'Comprar satoshis' ou 'Vender satoshis' de uma oferta, o [@lnp2pbot](https://t.me/lnp2pBot) responderá privadamente explicando o que você deve fazer para concluir o processo. 
Para que o bot possa responder à sua solicitação, é necessário que você o [inicialize](./how-do-i-initialize-the-bot.md), pois nenhum bot pode iniciar um chat com você se você não o tiver usado antes. Abra [@lnp2pbot](https://t.me/lnp2pBot) e digite o comando `/start` ou toque no botão 'Iniciar', depois tente aceitar o pedido novamente, volte ao bot e siga as instruções.
- Se você já usava o bot e a última vez foi antes de março de 2023, você precisa inicializá-lo novamente com o comando `/start`, pois foi reiniciado e os dados anteriores não foram preservados.

### Tentei pagar uma fatura com uma carteira sem fundos suficientes e agora o [@lnp2pbot](https://t.me/lnp2pbot) diz que a fatura foi usada

Aguarde 15 minutos para que o tempo da transação expire e inicie-a novamente para gerar uma nova fatura.

### Minha contraparte teve um problema ao me enviar o pagamento em moeda fiduciária e depois desapareceu, meus satoshis estão bloqueados

A transação será cancelada automaticamente após 23 horas e seus satoshis aparecerão em sua carteira como um pagamento falhado. Se você quiser acelerar o processo, pode abrir uma disputa com o comando `/dispute <ID do pedido>`.

### Um usuário aceitou minha compra por engano e eu já fiz o pagamento em satoshis

Você pode iniciar um cancelamento cooperativo. Ambos devem executar o comando `/cancel <ID do pedido>`.

### Cancelei um pedido, mas os satoshis ainda não voltaram para minha carteira. Quanto devo esperar?

Quando um pedido é cancelado, os satoshis do vendedor retornam imediatamente para o nó/carteira que realizou o pagamento. Se você usar uma carteira de auto-custódia ou seu próprio nó, não terá nenhum problema. Porém, se usar uma carteira que guarda seus fundos, você deve aguardar até que eles reflitam seu saldo no sistema interno, o que pode levar de alguns minutos a algumas horas, dependendo da carteira. No entanto, em todas as carteiras, 100% dos seus fundos retornarão, apenas seja paciente.

### Estou comprando e o bot não está me pedindo uma fatura, mas sim colocando-me diretamente em contato com o vendedor

Isso acontece quando você tem um endereço Lightning ativado. Nesse caso, os Satoshis que você compra são enviados diretamente para lá sem solicitar uma nova fatura em cada compra. Para verificar seu endereço Lightning, digite no [bot](https://t.me/lnp2pbot) o comando `/settings`, se quiser desativá-lo, digite no [bot](https://t.me/lnp2pbot) o comando `/setaddress off`.
