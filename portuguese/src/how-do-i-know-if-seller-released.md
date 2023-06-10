# Como posso saber se o vendedor realmente liberou os sats?

Se o @lnp2pBot lhe informar que o vendedor liberou, é porque realmente o fez, mas se você deseja verificar, pode fazer da seguinte forma:

Envie uma mensagem para o bot `/listorders` e, se o bot ainda estiver no processo de pagamento do seu pedido, o status que você verá será `PAID_HOLD_INVOICE`. Se o bot já tiver pago a fatura, o pedido não aparecerá na lista.

Quando um pedido tem o status `PAID_HOLD_INVOICE`, o vendedor não tem mais nenhuma responsabilidade, pois ele liberou os sats. Se você tiver problemas ao receber, vá para a seção [O vendedor liberou, mas não recebo os sats na minha carteira](./i-cant-receive.md).
