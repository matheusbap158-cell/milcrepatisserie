# Milcrê Pâtisserie (demo)

Landing page de demonstração, HTML único (`index.html`), sem dependências além das fontes do Google Fonts. Não publicada.

## Estrutura
- `index.html`: o site (hero com vitrine de fotos, manifesto, coleções com catálogos, galeria com zoom, ferramenta "Monte a sua mesa" com cartão-convite, história da Simara, como encomendar, avaliações, contato com mapa)
- `Copy.txt`: texto da página
- `design-system-milcre.md` / `.html`: design system
- `assets/`: logo dourada (e a versão clara para fundo escuro), fotos otimizadas, favicon e imagem de compartilhamento
- `Logo/`, `Imagens/`, `Fotos/`, `Sobre a Simara Velácio/`, `Info para copy/`, `Link do ...txt`: materiais de origem

## Como visualizar
Na pasta da agência: `node "_ferramentas/preview-local.mjs" "4. Meus Clientes/2. Demos e propostas/milcrepatisserie"` e abrir o endereço mostrado. Dica: se o navegador de teste deixar a aba em segundo plano (`document.visibilityState` igual a `hidden`), as animações e capturas congelam; abrir uma aba nova e ativa resolve.

## Antes de publicar
- O `index.html` tem `<meta name="robots" content="noindex, nofollow">` para a demo não aparecer no Google. Remover ao publicar o site definitivo.
- Os itens `[A CONFIRMAR]` aparecem no site com borda tracejada; a lista completa está na ficha em `4. Meus Clientes/_Fichas/Milcre Patisserie.pdf`.
- Os botões de catálogo levam ao Linktree; trocar pelos links diretos dos PDFs do Drive quando a cliente enviar.
- A Simara precisa aprovar o texto (adaptado para a primeira pessoa) e autorizar o retrato e as fotos.
- Conferir autoria das fotos (fotógrafo e eventos de clientes) e autorização das avaliações (usadas só com as iniciais).
- A logo veio com 150 px; pedir o arquivo em alta resolução (ou vetorial).
