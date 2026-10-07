# CriaKit

Estúdio de edição de vídeo que roda no seu computador, dentro do Claude Code e do Codex.

Este repositório serve **apenas para distribuir os arquivos de instalação**. O código-fonte não está aqui.

## Instalação

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

## Licença

O estúdio é um fork do [HyperFrames](https://github.com/heygen-com/hyperframes) (Apache-2.0).
O motor do CriaKit é proprietário: a instalação exige uma chave de acesso válida.
