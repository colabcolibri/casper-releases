# Casper — releases públicas do desktop

Este repositório hospeda **somente artefatos de distribuição** do app desktop **Casper** (Windows e macOS). O código-fonte fica em um repositório privado; aqui publicamos instaladores, o manifesto de auto-update (`latest.json`) e pacotes assinados do updater quando aplicável.

**README em inglês:** [README.md](README.md)

## Download (recomendado)

Use os links **oficiais** do site — sempre apontam para a release mais recente, sem precisar navegar no GitHub:

| Plataforma | Link |
| ---------- | ------------------------------------------------ |
| Windows | https://casper.sergioluciano.com/download/windows |
| macOS | https://casper.sergioluciano.com/download/mac |

Site: https://casper.sergioluciano.com  
Demo no navegador: https://demo.casper.sergioluciano.com

## Releases neste repositório

Na aba **[Releases](https://github.com/colabcolibri/casper-releases/releases)**, cada tag `desktop-v*` (semver com prefixo) inclui:

- **Windows:** `Casper_*-setup.exe` (instalador NSIS)
- **Windows (updater):** `latest.json`, `*.nsis.zip` e `*.sig` correspondente quando o updater está habilitado
- **macOS:** `.dmg` na mesma release quando um build Mac é enviado

### Como os builds chegam aqui

| Plataforma | Pipeline |
| ---------- | -------- |
| Windows | GitHub Actions no repo privado de código — push da tag `desktop-v*` |
| macOS | Build assinado local no Mac → `pnpm publish:desktop:mac --upload` |

## Trial e licença

- **Trial de 7 dias:** inicie pelo app — na primeira abertura, informe seu e-mail (o desktop envia a solicitação ao license-server).
- **Licença paga:** após a compra no site, você recebe um **código de licença por e-mail**. Digite na tela de ativação do app.
- O **demo no navegador** em `demo.casper.sergioluciano.com` é somente leitura e não exige licença desktop.

## Suporte

Dúvidas de compra ou download: canais listados no site oficial. Este repositório **não** trata problemas do produto — só hospeda os binários de release.
