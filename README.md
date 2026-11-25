# LucreShop

Plugin oficial do LucreShop para assistentes de IA. Use sua conta do LucreShop para trabalhar no projeto autorizado. Hoje o plugin cuida das campanhas de envio de ofertas: escolher ofertas, revisar a fila e acompanhar importações.

## Conectar

No Claude Desktop, baixe o pacote para Claude e siga as instruções de instalação do guia. [Guia de instalação](https://app.lucreshop.com.br/downloads/plugin/guia.html)

No Claude Code, adicione o marketplace do LucreShop e instale o plugin:

```
/plugin marketplace add Alberto-Monteiro/lucreshop-plugin
/plugin install lucreshop@lucreshop
```

No Codex, adicione o marketplace e instale **LucreShop** em `/plugins`:

```
codex plugin marketplace add Alberto-Monteiro/lucreshop-plugin
```

No Gemini CLI, instale a extensão e entre com `/mcp auth lucreshop`:

```
gemini extensions install https://github.com/Alberto-Monteiro/lucreshop-plugin
```

No Antigravity CLI, instale o plugin e autentique o servidor do LucreShop em `/mcp`:

```
agy plugin install https://github.com/Alberto-Monteiro/lucreshop-plugin
```

Abra a conexão **lucreshop** e entre no LucreShop para escolher o projeto e as permissões. Ative **Ofertas dos marketplaces** para preparar prévias e importar as ofertas escolhidas. Para desfazer um lote, a conexão também precisa de **Limpeza de fila**. Você pode consultar ou revogar o acesso no painel do LucreShop. [Conexões de IA](https://app.lucreshop.com.br/settings/conexoes-ia)

## Pedidos para experimentar

- “Na campanha de maternidade, prepare uma prévia com 20 ofertas da Shopee. Mostre o preço e o vendedor de cada oferta e aguarde minha escolha.”
- “Mostre os próximos 10 itens da fila da campanha de maternidade e explique o estado de cada um.”
- “Encontre a última importação da Magalu que adicionou ofertas à campanha de maternidade. Mostre quantas entraram e quantas eram duplicadas.”
- “Mostre os itens que selecionei na fila de maternidade e aguarde minha confirmação antes de excluir.”
- “Prepare o reenvio dos itens finalizados da campanha de maternidade. Mostre quantos voltariam à fila.”
- “Prepare a ambientação da foto do item que escolhi. Gere somente o cenário com minha ferramenta de imagem e abra a comparação no LucreShop.”
- “Mostre a foto atual e esta nova imagem lado a lado. Aguarde minha aprovação antes de trocar a foto.”

A busca da Magalu consulta a vitrine Magazine Você do projeto. Se faltarem produtos, a prévia também aceita anúncios que você abriu no seu navegador. Uma prévia já salva pode ser consultada em outro chat pelo identificador.

Para ambientar a foto, use uma ferramenta de imagem disponível na sua conta ou selecione um cenário que você já criou. O navegador compõe o recorte da foto atual com o cenário e mostra as duas versões. A imagem entra no item da fila quando você aprova no painel autenticado.

Você também pode enviar uma imagem completa a partir da sua ferramenta, comparar com a foto atual e aprovar a troca em um produto da prévia ou em um item da fila que ainda não teve tentativa de envio. Para enviar pelo MCP, use PNG, JPEG ou WebP de até 10 MB e pelo menos 200 px por lado, como arquivo em Base64 ou link HTTPS direto. O LucreShop redimensiona a imagem para até 1.600 px e aplica a troca após sua confirmação. A troca em um item da fila requer **Gestão de campanhas**.

## Se a conexão pedir atenção

Se o projeto esperado não aparecer, confira qual projeto foi autorizado em **Conexões de IA**. Se a autorização terminar em erro, registre o horário e o nome da ferramenta para que o suporte identifique o pedido. [Suporte LucreShop](https://app.lucreshop.com.br/downloads/plugin/guia.html#suporte)
