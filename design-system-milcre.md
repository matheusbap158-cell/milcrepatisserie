# Design system: Milcrê Pâtisserie

Base: a logo dourada com a flor-de-lis e o monograma, a placa de vidro do ateliê (letras marrom-cacau, fios dourados e a frase "Ateliê de doces finos") e as fotos dos doces (cerejas ao chocolate, lavanda, folha de ouro, flores de açúcar). É alta confeitaria: o produto é o protagonista e a página precisa soar como uma vitrine de ateliê, não como um site de loja.

## Tom visual (3 linhas)
1. Editorial e silencioso: marfim, dourado fosco e cacau escuro, muito espaço e fotos grandes.
2. Tipografia serifada de alto contraste, com itálico nas palavras de emoção, e rótulos finos em caixa alta espaçada, como a placa.
3. Detalhes de ourivesaria: fios dourados, a flor-de-lis como divisor e um cartão-convite dourado na ferramenta de pedido.

## 1. Cores

| Papel | Token | Hex | Uso |
|---|---|---|---|
| Marfim | --ivory-50 | #FBF8F3 | Fundo padrão |
| Champagne | --champagne-100 | #F3EADB | Seções alternadas, cartões |
| Champagne escuro | --champagne-200 | #E6D6BC | Bordas e fundos de chip |
| Dourado fosco | --gold-500 | #B8964E | Fios, ícones e detalhes (não é cor de texto) |
| Dourado texto | --gold-700 | #7A6038 | Texto dourado sobre marfim (contraste 5,7:1) |
| Dourado claro | --gold-300 | #D8B878 | Dourado sobre fundo escuro (contraste 9:1) |
| Cacau | --cocoa-900 | #24150F | Seções escuras, botão primário, texto forte |
| Cacau 2 | --cocoa-800 | #33211A | Cartões sobre fundo escuro |
| Cacau 3 | --cocoa-700 | #4A3126 | Bordas sobre fundo escuro |
| Cereja | --cherry-700 | #8A1C2E | Único acento forte (selo e destaques pequenos) |
| Lavanda | --lav-500 | #7E62B0 | Detalhe raro, só em ilustração |
| Tinta | --ink | #2A1D17 | Texto de corpo |
| Texto secundário | --muted | #6B5A4E | Apoio (contraste 6,3:1) |
| Linha | --line | #E4D6BE | Divisores |
| WhatsApp | --wa-500 | #25D366 | **Exclusivo** do botão e do flutuante (texto escuro #24150F) |
| Alerta | --alert-600 | #B3261E | Erro de formulário |

Regras: o dourado de texto sobre marfim é sempre o #7A6038; o #B8964E só em fios e ícones. Cereja nunca em bloco grande. O verde do WhatsApp nunca é decorativo e leva texto escuro.

## 2. Tipografia

| Uso | Fonte | Peso |
|---|---|---|
| Títulos | Cormorant Garamond (com itálico) | 500 e 600 |
| Corpo e rótulos | Jost | 300, 400 e 500 |

Link de fontes: `https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,500;0,600;1,500;1,600&family=Jost:wght@300;400;500&display=swap`

Hierarquia (desktop / mobile):
- H1: 76 px / 42 px, peso 500, entrelinha 1,02, espaçamento -0,01em; palavras de emoção em itálico
- H2: 54 px / 36 px, peso 500, entrelinha 1,08
- H3: 28 px / 24 px, peso 600
- Corpo: 18 px / 16 px, Jost 300 a 400, entrelinha 1,75
- Rótulo (caixa alta): 12,5 px, Jost 500, espaçamento 0,22em
- Botão: 14 px, Jost 500, caixa alta, espaçamento 0,14em

## 3. Componentes

**Botão primário (fundo marfim):** cacau, texto marfim, 56 px, raio 2 px (quase reto, como a placa). Hover: sobe 2 px e o fio dourado aparece embaixo.
**Botão primário (fundo escuro):** dourado claro com texto cacau.
**Botão secundário:** contorno dourado de 1 px, texto da cor da seção.
**Botão WhatsApp:** verde #25D366 com texto cacau, mesmo formato dos demais.
**Cartão de coleção:** foto alta, borda de 1 px na cor da linha, canto reto, título serifado e link com seta. Hover: a foto dá um leve zoom.
**Chip de escolha:** retângulo fino com borda dourada; selecionado = fundo cacau, texto marfim e um pequeno "✓".
**Controle de convidados:** trilho fino dourado e marcador redondo em cacau, com o número grande em serifada.
**Cartão-convite:** marfim, moldura dupla dourada, flor-de-lis no topo e selo "M" em cereja.
**Campos:** fundo marfim, só a linha de baixo, foco com linha dourada grossa.
**Placeholder de pendência:** borda tracejada com "[A CONFIRMAR]", sempre visível.

## 4. Estética
- Raios: 2 px nos botões e cartões (o contrário de "fofo"), 999 px só em bolinhas e selos.
- Sombras: quase nenhuma; profundidade vem de fio dourado, foto grande e fundo cacau.
- Espaçamento (base 8): 8, 16, 24, 32, 48, 80, 128 px. Seções amplas, com muito ar.
- Forma assinatura: a flor-de-lis entre dois fios dourados, que separa as seções.
- Movimento: fotos do hero em transição lenta, revelação suave ao rolar, brilho dourado discreto nos títulos, galeria que desliza. Tudo desligado com `prefers-reduced-motion`.

## 5. Conversão para WhatsApp
- CTA no topo, no hero, na ferramenta "Monte a sua mesa" (a mensagem já vai pronta), em "Como encomendar", na seção da Simara, no contato e no fim.
- A ferramenta transforma ocasião, convidados, data e itens num cartão-convite e leva tudo para o WhatsApp da Milcrê.
- Botões para os catálogos e para a encomenda online mantêm as duas portas já usadas pela marca.
- Autoridade: "desde 2017", a história dela em primeira pessoa, as fotos reais do ateliê e as avaliações do Google.
- Sem preço e sem promessa de prazo.

## Tokens prontos (CSS)

```css
:root{
  --ivory-50:#FBF8F3; --champagne-100:#F3EADB; --champagne-200:#E6D6BC;
  --gold-300:#D8B878; --gold-500:#B8964E; --gold-700:#7A6038;
  --cocoa-900:#24150F; --cocoa-800:#33211A; --cocoa-700:#4A3126;
  --cherry-700:#8A1C2E; --lav-500:#7E62B0;
  --ink:#2A1D17; --muted:#6B5A4E; --line:#E4D6BE;
  --wa-500:#25D366; --alert-600:#B3261E;
  --font-display:'Cormorant Garamond',Georgia,serif;
  --font-body:'Jost',-apple-system,'Segoe UI',sans-serif;
  --r-sm:2px; --r-pill:999px;
}
```
