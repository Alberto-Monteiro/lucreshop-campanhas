---
name: revisar-fila
description: Consulta o estado e a fila de uma campanha do LucreShop. Use para ver os próximos itens, sua ordem, os totais da campanha ou conferir se uma importação alterou a fila.
---

Localize a campanha com `listar_campanhas` e confira o nome do projeto autorizado. Se houver campanhas com nomes semelhantes e o pedido for ambíguo, apresente as opções antes de continuar.

Leia a fila com `consultar_fila`. Para os próximos itens, use o limite solicitado e respeite a ordem informada pela ferramenta. Para a fila inteira, avance o `offset` pelo número de itens recebidos até `temMais` ser falso. Informe o estado da campanha, o total retornado e os itens solicitados. A mensagem da listagem é um trecho.

Se a pessoa quiser conferir uma importação entre chats, consulte também o recibo correspondente. Compare os `queueItemIds` do recibo com os IDs da fila quando necessário. Uma campanha ativa pode consumir itens entre duas consultas, por isso a diferença no total por si só é insuficiente para atribuir uma inclusão ou duplicata ao pedido.
