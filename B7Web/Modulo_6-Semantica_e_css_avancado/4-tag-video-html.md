# Guia Completo da Tag `<video>` em HTML

## O que é a tag `<video>`?

A tag `<video>` em HTML é usada para incorporar vídeos diretamente nas páginas web, permitindo que os usuários assistam ao conteúdo multimídia sem precisar usar plugins externos.

Ela fornece uma maneira fácil e padronizada de adicionar vídeos, com suporte a controles, legendas, múltiplas fontes e até fallback (alternativas) para navegadores que não suportam o elemento.

---

## Estrutura básica da tag `<video>`

```html
<video src="caminho/do/video.mp4" controls>
  Seu navegador não suporta o elemento de vídeo.
</video>
```

Ou utilizando múltiplas fontes:

```html
<video controls>
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
  <source src="video.ogg" type="video/ogg">
  Seu navegador não suporta o elemento de vídeo.
</video>
```

---

## Atributos da tag `<video>`

- `src`: Caminho para o arquivo de vídeo.
- `controls`: Exibe os controles de reprodução (play, pause, volume, etc.).
- `autoplay`: O vídeo começa a reproduzir automaticamente quando carregado (pode ser bloqueado por alguns navegadores).
- `loop`: Faz o vídeo reiniciar automaticamente quando termina.
- `muted`: Inicia o vídeo sem som.
- `poster`: Especifica uma imagem a ser exibida antes do vídeo começar (thumbnail).
- `preload`: Indica como o navegador deve carregar o vídeo.
  - `none`: Não carrega nada até que o usuário interaja.
  - `metadata`: Carrega apenas metadados (duração, dimensões, etc.).
  - `auto`: Carrega todo o vídeo automaticamente (padrão).
- `width`: Define a largura do player.
- `height`: Define a altura do player.
- `playsinline`: Permite que o vídeo seja reproduzido em linha em dispositivos móveis (em vez de ir para tela cheia).

---

## Exemplo completo com todos os atributos

```html
<video width="640" height="360" controls autoplay loop muted poster="imagem-thumbnail.jpg" preload="metadata">
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
  <source src="video.ogg" type="video/ogg">
  Seu navegador não suporta vídeos HTML5.
</video>
```

---

## Exemplo com vídeo em reprodução automática e sem som

```html
<video src="video.mp4" autoplay muted playsinline></video>
```

---

## Exemplo com imagem de capa (poster)

```html
<video src="video.mp4" controls poster="capa.png"></video>
```

---

## Fallback (conteúdo alternativo)

Se o navegador não suporta a tag `<video>`, você pode exibir uma mensagem ou link alternativo:

```html
<video src="video.mp4" controls>
  Seu navegador não suporta vídeo. <a href="video.mp4">Baixe o vídeo aqui</a>.
</video>
