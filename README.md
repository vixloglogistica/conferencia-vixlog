# Conferência de Crossdocking — Vix Log

App de conferência (bipagem) do crossdocking para coletores Bluebird e tablets. O dia de trabalho tem 3 etapas, uma aba para cada:

1. **Entrada** — bipar as caixas que chegam, conferindo contra o relatório de entrada em PDF, e guardar nos paletes.
2. **Separação** — montar cada pedido de uma transportadora, pegando as caixas nos paletes.
3. **Expedição** — bipar as caixas ao carregar o caminhão e fechar o romaneio.

Todos os coletores da equipe trabalham ao mesmo tempo no mesmo relatório. Ao final de cada etapa o app gera o PDF (checklist ou romaneio), guarda no Drive e registra na planilha de controle.

Funciona como atalho (PWA): este repositório é só a "casca" (GitHub Pages) que abre o app hospedado no Google Apps Script.

## Endereço do app
`https://vixloglogistica.github.io/conferencia-vixlog/`

## Arquivos deste repositório
- `index.html` — tela de abertura + app em tela cheia (precisa da `APP_URL` do Apps Script)
- `manifest.json`, `sw.js`, `icones/` — instalação como atalho, ícones da marca
- `manual/Manual-Conferencia-Crossdocking-VixLog.pdf` — manual de uso para os conferentes (a primeira página traz o QR code de instalação)
- `manual/qr.png` — QR code do endereço do app

## Instalar nos aparelhos
Leia o QR code do manual (`manual/qr.png`) com a câmera, ou abra `vixloglogistica.github.io/conferencia-vixlog` no Chrome do coletor/tablet → menu ⋮ → **Adicionar à tela inicial**. O app abre pela internet e está sempre atualizado; as leituras ficam guardadas no aparelho quando o sinal cai e são enviadas quando a internet volta.

## Ligar a casca ao app
No `index.html`, a constante `APP_URL` guarda a URL `/exec` da implantação do Apps Script. Se a implantação mudar de URL, troque ali e faça commit.
