# CriaKit

Estúdio de edição de vídeo e criação de carrossel que roda **no seu computador**, dentro do Claude ou do ChatGPT.

Este repositório serve **apenas para distribuir os arquivos de instalação**. O código-fonte não está aqui.

## Instalação sem terminal (Mac com chip Apple)

Baixe em [releases/latest](https://github.com/faabricioleite/criakit/releases/latest) e abra o arquivo:

| Onde você usa | Arquivo | O que fazer |
| --- | --- | --- |
| **Claude Desktop** | `criakit-…-darwin-arm64.mcpb` | abra o arquivo e confirme a instalação; cole a sua chave quando ele pedir |
| **ChatGPT desktop** | `criakit-…-darwin-arm64-chatgpt.zip` | descompacte e siga o `LEIA-ME.txt` de dentro |

Os dois já vêm com tudo: não precisa instalar Node, ffmpeg nem nada.

## Instalação pelo comando (Mac, Windows e Linux)

**Claude Code**

```bash
claude mcp add --scope user criakit -e CRIAKIT_CHAVE=SUA_CHAVE -- \
  npx -y https://github.com/faabricioleite/criakit/releases/latest/download/criakit.tgz
```

**Codex**

```bash
codex mcp add criakit --env CRIAKIT_CHAVE=SUA_CHAVE -- \
  npx -y https://github.com/faabricioleite/criakit/releases/latest/download/criakit.tgz
```

**Windows (Claude Code)**

```bash
claude mcp add --scope user criakit -e CRIAKIT_CHAVE=SUA_CHAVE -- \
  cmd /c npx -y https://github.com/faabricioleite/criakit/releases/latest/download/criakit.tgz
```

Troque `SUA_CHAVE` pela chave que você recebeu por e-mail na compra.

## Como usar

Depois de instalar, peça na conversa:

> edite esse vídeo: /caminho/do/seu/video.mov

O CriaKit abre o arquivo, acha onde você fala, tira as pausas, monta a linha do tempo e abre o
estúdio no navegador — tudo no seu computador. O vídeo original nunca é alterado e nunca sai da
sua máquina.

Para carrossel:

> cria um carrossel sobre …

## Legenda automática: onde funciona

A transcrição (que é o que permite cortar erro de fala, e não só silêncio) vem dentro do pacote em
**Mac com chip Apple** e **Windows 64 bits**. Em **Mac Intel** ela ainda não vem: o corte por silêncio
funciona e a IA avisa.

No Windows, se aparecer erro de uma DLL faltando (`VCRUNTIME140.dll` e parentes), instale o
[Visual C++ Redistributable](https://aka.ms/vs/17/release/vc_redist.x64.exe) da Microsoft — quase toda
máquina já tem, e é um clique.

## Licença

O estúdio é um fork do [HyperFrames](https://github.com/heygen-com/hyperframes) (Apache-2.0).
O motor do CriaKit é proprietário: a instalação exige uma chave de acesso válida.
