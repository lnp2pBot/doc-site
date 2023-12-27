# Completando uma ordem

Muitas disputas são iniciadas porque uma das partes demorou a responder uma mensagem, houve um mal-entendido ou um atraso em algum pagamento. Esses são casos simples que requerem apenas paciência e colaboração na comunicação. Outros casos envolvem má fé, como um vendedor que quer ficar com o dinheiro fiat e receber os sats de volta. Para esses casos, o solver pode executar o comando `/settleorder`, o que faz com que reconheça o pagamento recebido e envie automaticamente os sats para o comprador.

![Completando uma ordem](./assets/images/settleorder.png)

## Completando uma ordem quando o fiat demora para chegar
Com o [@lnp2pbot](https://t.me/lnp2pBot), devem-se utilizar métodos de pagamento que garantam o envio instantâneo do fiat. No entanto, pode haver casos em que o fiat demore mais do que o habitual para chegar ao vendedor de sats, por exemplo, devido a problemas no processamento do pagamento pelo banco.
Em tais situações, o comprador corre o risco de o vendedor não receber o fiat [antes que a hold invoice expire](./how-long-does-it-take-to-finalize-a-transaction.md) e, portanto, não liberar os sats. Porém, quando a hold invoice expirar, o vendedor terá os sats de volta, e depois o fiat. O comprador ficaria à mercê da boa vontade do vendedor, que poderia ou não enviar os satoshis, sem que o bot possa intervir. Para evitar isso, os usuários podem recorrer aos solvers de sua comunidade, que atuarão como mediadores.

Um solver pode fazer com que o bot congele a hold invoice do vendedor usando o comando `/freezeorder <order_id>`, então podem esperar o tempo suficiente para o fiat chegar e, quando isso acontecer, o solver liberará os sats com o comando `/paytobuyer <order_id>`. É possível que a fatura do comprador tenha expirado durante o processo, então eles devem atualizá-la digitando `/setinvoice <order id> <lightning invoice>`.

Essa solução implica a custódia dos sats pelo bot e deve ser usada apenas quando não houver outras opções.
