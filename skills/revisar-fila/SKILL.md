---
name: revisar-fila
description: Consulta o estado e a fila de uma campanha do LucreShop. Use para ver os próximos itens, sua ordem, os totais da campanha entender um bloqueio, revisar uma limpeza ou conferir se uma importação alterou a fila.
---

Localize a campanha com `listar_campanhas` e confira o nome do projeto autorizado. Se houver campanhas com nomes semelhantes e o pedido for ambíguo, apresente as opções antes de continuar.

Leia a fila com `consultar_fila`. Para os próximos itens, use o limite solicitado e respeite a ordem informada pela ferramenta. Para a fila inteira, avance o `offset` pelo número de itens recebidos até `temMais` ser falso. Informe o estado da campanha, o total retornado e os itens solicitados. A mensagem da listagem é um trecho. Filtre por `estado` quando a pessoa pedir um grupo. Para itens afetados por revalidação, explique o `motivo` quando estiver disponível. Use `consultar_item_fila` para conferir o histórico.

Se a pessoa quiser conferir uma importação entre chats, consulte também o recibo correspondente. Compare os `queueItemIds` do recibo com os IDs da fila quando necessário. Uma campanha ativa pode consumir itens entre duas consultas, por isso a diferença no total por si só é insuficiente para atribuir uma inclusão ou duplicata ao pedido.

Para limpar, chame `preparar_limpeza_fila` com o grupo escolhido. Mostre as contagens por estado e os itens em envio que serão preservados. Só chame `limpar_fila` com o `confirmationId` da mesma prévia depois de uma aprovação explícita. Se a confirmação expirar ou a fila mudar, gere outra prévia e aguarde nova aprovação.
