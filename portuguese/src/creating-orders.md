# Criando ordens

O funcionamento do bot continua exatamente o mesmo, por padrão ele cria ordens em um canal global. No entanto, como criamos uma nova comunidade, queremos que nossa ordem seja publicada no canal associado a essa comunidade. Existem duas maneiras de criar uma ordem na nova comunidade.

1. Entramos no grupo da comunidade (no caso do nosso exemplo, seria @p2pZimbabwe) e dentro do grupo executamos o comando usual: `/sell` ou `/buy`.
2. Se preferirmos algo mais privado, informamos ao bot nossa comunidade padrão executando o comando `/setcomm @p2pZimbabwe`. A partir desse momento, todas as ordens que criarmos em particular irão para o canal correspondente vinculado ao @p2pZimbabwe. Podemos alterar nossa comunidade padrão quando desejarmos com `/setcomm @ComunidadeMuitoLegal` (exemplo). Também podemos voltar ao estado anterior, onde não tínhamos uma comunidade padrão, executando `/setcomm off`.
