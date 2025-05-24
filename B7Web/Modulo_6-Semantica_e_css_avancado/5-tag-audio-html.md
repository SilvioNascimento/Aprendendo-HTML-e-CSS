# Guia Completo da Tag `<audio>` em HTML

## O que é a tag `<audio>`?

A tag `<audio>` permite incorporar arquivos de áudio diretamente em páginas HTML, permitindo que os usuários ouçam músicas, podcasts, efeitos sonoros e outros conteúdos sonoros sem precisar de plugins externos.

Ela suporta múltiplas fontes de áudio e controles para reprodução, pausa, volume, entre outros.

---

## Estrutura básica da tag `<audio>`

```html
<audio src="audio.mp3" controls>
  Seu navegador não suporta o elemento de áudio.
</audio>
```

Ou com múltiplas fontes usando a tag `<source>`:

```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg" />
  <source src="audio.ogg" type="audio/ogg" />
  Seu navegador não suporta áudio HTML5.
</audio>
```

---

## Atributos da tag `<audio>`

- `src`: Caminho para o arquivo de áudio (pode ser omitido se usar `<source>`).
- `controls`: Exibe controles nativos do player (play, pause, volume).
- `autoplay`: Inicia a reprodução automaticamente após o carregamento (pode ser bloqueado por navegadores).
- `loop`: Reproduz o áudio em loop contínuo.
- `muted`: Inicia o áudio silenciado.
- `preload`: Indica ao navegador como deve carregar o áudio antes da reprodução.
  - `none`: Não carrega nada antes da interação do usuário.
  - `metadata`: Carrega apenas os metadados (duração, etc.).
  - `auto`: Carrega o áudio inteiro automaticamente.
- `width` e `height`: Não aplicáveis na tag `<audio>`.
- `crossorigin`: Controla a política de CORS para fontes externas.
- `playsinline`: Em áudio, geralmente não utilizado.

---

## Exemplo completo com múltiplas fontes e controles

```html
<audio controls autoplay loop preload="metadata" muted>
  <source src="musica.mp3" type="audio/mpeg" />
  <source src="musica.ogg" type="audio/ogg" />
  <source src="musica.wav" type="audio/wav" />
  Seu navegador não suporta áudio HTML5.
</audio>
```

---

## Suporte a formatos comuns

- `.mp3` (audio/mpeg) — amplamente suportado
- `.ogg` (audio/ogg) — formato aberto, bom suporte
- `.wav` (audio/wav) — áudio sem compressão, maior tamanho

---

## Fallback (conteúdo alternativo)

Se o navegador não suportar a tag `<audio>`, você pode exibir uma mensagem ou link para download:

```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg" />
  Seu navegador não suporta áudio. <a href="audio.mp3">Baixe o arquivo aqui</a>.
</audio>
