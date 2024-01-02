# Como saber se o vendedor realmente liberou os sats?

Se o @lnp2pBot disser que o vendedor liberou, é porque realmente o fez, mas se você quiser verificar, pode fazer da seguinte maneira:

Digite para o bot `/listorders` e se o bot ainda estiver no processo de pagar sua fatura, o status que você verá será `PAID_HOLD_INVOICE`, se o bot já pagou a fatura, a ordem não aparecerá na lista.

Quando uma ordem tem o status `PAID_HOLD_INVOICE`, o vendedor não tem mais nenhuma responsabilidade, pois já liberou os sats. Se você tiver problemas para receber, vá para a seção [O vendedor liberou, mas os sats não estão chegando à minha carteira](./i-cant-receive.md).
