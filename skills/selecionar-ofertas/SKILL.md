---
name: selecionar-ofertas
description: Prepara uma prévia numerada de ofertas da Shopee, Mercado Livre, Amazon ou Magalu para uma campanha LucreShop. Use quando a pessoa quiser escolher produtos, conferir a mensagem ou importar itens de uma prévia.
---

Resolva o nome com `listar_campanhas` no LucreShop. Confira o projeto autorizado e peça a escolha se houver mais de uma campanha possível.

1. Se já houver um `previewId`, recupere a prévia salva da loja. Para uma busca nova, use a ferramenta de preparar prévia da loja com o nicho e a quantidade pedidos. Na Magalu, a ferramenta recebe ofertas observadas no navegador do usuário. Se faltar acesso ao navegador, use uma prévia existente ou solicite os dados das ofertas. Registre o preço e as condições conforme apresentados pela loja.
2. Apresente as ofertas na ordem da prévia, numeradas a partir de 1, com título, vendedor e preço quando disponíveis. Identifique condições como Pix, cupom e “a partir de”. Informe o `previewId` para a pessoa poder continuar em outro chat. Para mostrar a divulgação de um item, chame `visualizar_mensagem_oferta` e apresente a mensagem, imagem, preço, condições e resultado da conversão.
3. Aguarde a escolha da pessoa. Mapeie os números escolhidos para os IDs da mesma prévia, preservando a ordem da seleção e o vendedor. Na Shopee envie o `selectionId` completo (`shopId:itemId`), no Mercado Livre o ID do anúncio MLB, na Amazon o ASIN e na Magalu o `itemId`.
4. Ao importar, use a ferramenta de seleção da loja com `campaignId`, `previewId`, `itemIds` e um `requestId` próprio do pedido. Se repetir a operação em outro cliente ou após uma interrupção, reutilize todos esses valores. Use o recibo para informar quantas ofertas entraram, quantas eram duplicadas e quais foram recusadas. Inclua os identificadores da prévia e do pedido.
