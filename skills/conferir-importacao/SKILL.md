---
name: conferir-importacao
description: Localiza lotes e recibos de importação de ofertas no LucreShop e permite desfazer os itens elegíveis de um lote após revisar o impacto. Use para consultar histórico, conferir duplicatas ou retirar uma importação específica.
---

Resolva o nome da campanha com `listar_campanhas` no projeto autorizado. Caso o nome identifique mais de uma campanha, peça a escolha da pessoa.

Para localizar um pedido, use `listar_importacoes_campanha` com os filtros de loja e data solicitados. Para “o último lote que adicionou itens”, use `apenasComAdicoes: true` e `limite: 1`. Use o `requestId` retornado para consultar o recibo da loja. Na Shopee, consulte `consultar_importacao_selecao_shopee` para uma seleção com prévia e `consultar_importacao` para uma importação por busca. Diferencie as quantidades adicionadas, duplicadas e recusadas na gravação original das retiradas registradas posteriormente.

Se a pessoa solicitar que um lote seja desfeito, use o `batchId` do histórico com `preparar_desfazer_importacao`. Mostre o lote, a quantidade adicionada originalmente, os IDs que podem ser retirados e a quantidade preservada. Quando houver itens elegíveis, aguarde confirmação explícita da pessoa sobre essa prévia antes de usar `desfazer_importacao` com o `confirmationId` recebido. Se a fila tiver mudado e o servidor pedir nova prévia, apresente o impacto atualizado e peça nova confirmação. Relate os IDs retirados pelo servidor.
