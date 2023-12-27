# Trocas Seguras no @lnp2pbot

O @lnp2pbot é uma ferramenta segura para a troca de Bitcoin de forma P2P sem KYC. Quando duas pessoas se conectam para realizar uma compra ou venda, os Satoshis (Sats) do vendedor são retidos em sua própria carteira por meio de uma fatura retida (hold invoice) e não podem ser utilizados enquanto estiverem nesse estado. Quando o comprador de Sats enviar o dinheiro fiat e o vendedor confirmar ao bot que o recebeu, os Sats serão enviados para o nó do bot e este os pagará ao comprador o mais rápido possível.

O bot possui um sistema de [reputação de usuários](https://lnp2pbot.com/aprende/how-does-the-user-reputation-system-work.html) que leva em consideração a quantidade de operações bem-sucedidas e as avaliações recebidas. Além disso, exibe a quantidade de dias que uma pessoa tem utilizado o serviço. Esses dados podem ajudar na tomada de decisão sobre aceitar ou rejeitar ofertas de acordo com seus próprios interesses.

Além disso, cada comunidade no bot possui pelo menos um Solver, responsável por mediar disputas que possam surgir. Esse Solver solicitará as provas necessárias às partes envolvidas e determinará quem está correto, recebendo assim os Sats. Quando um fraudador é detectado, ele é permanentemente banido e proibido de continuar utilizando o bot.
