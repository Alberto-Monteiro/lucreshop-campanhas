---
name: revisar-fila
description: Consulta o estado e a fila de uma campanha do LucreShop. Use para ver itens e bloqueios, revisar uma limpeza, excluir itens selecionados, preparar reenvios ou ambientar a foto de uma oferta para aprovação.
---

Localize a campanha com `listar_campanhas` e confira o nome do projeto autorizado. Se houver campanhas com nomes semelhantes e o pedido for ambíguo, apresente as opções antes de continuar.

Leia a fila com `consultar_fila`. Para os próximos itens, use o limite solicitado e respeite a ordem informada pela ferramenta. Para a fila inteira, avance o `offset` pelo número de itens recebidos até `temMais` ser falso. Informe o estado da campanha, o total retornado e os itens solicitados. A mensagem da listagem é um trecho. Filtre por `estado` quando a pessoa pedir um grupo. Para itens afetados por revalidação, explique o `motivo` quando estiver disponível. Use `consultar_item_fila` para conferir o histórico.

Se a pessoa quiser conferir uma importação entre chats, consulte também o recibo correspondente. Compare os `queueItemIds` do recibo com os IDs da fila quando necessário. Uma campanha ativa pode consumir itens entre duas consultas, por isso a diferença no total por si só é insuficiente para atribuir uma inclusão ou duplicata ao pedido.

Para limpar, chame `preparar_limpeza_fila` com o grupo escolhido. Mostre as contagens por estado e os itens em envio que serão preservados. Só chame `limpar_fila` com o `confirmationId` da mesma prévia depois de uma aprovação explícita. Se a confirmação expirar ou a fila mudar, gere outra prévia e aguarde nova aprovação.

Para excluir uma seleção, resolva a escolha nos IDs retornados por `consultar_fila` e chame `preparar_exclusao_itens_fila`. Mostre os itens que serão removidos e os que estão em envio. Depois de confirmar, chame `excluir_itens_fila` com o `confirmationId` da prévia.

Para reenviar, chame `preparar_reenvio_fila` com `todos` para toda a fila ou `selecionados` com os IDs escolhidos. Mostre quais itens finalizados voltam a pendente e informe se a campanha está ativa ou pausada. Após aprovação, chame `reenviar_itens_fila` com o mesmo grupo e `confirmationId`. A campanha pausada permanece pausada.

Para ambientar a foto de um item, use `preparar_ambientacao_imagem_fila`. Use a ferramenta de imagem habilitada pelo usuário para gerar somente o cenário, com espaço para a foto original. Entregue o arquivo do cenário e abra o link de revisão. O painel compõe o recorte da foto com o fundo gerado e mostra os dois lados. Peça ao usuário para aprovar no painel. Use `consultar_item_fila` para verificar qual foto ficou no item.
