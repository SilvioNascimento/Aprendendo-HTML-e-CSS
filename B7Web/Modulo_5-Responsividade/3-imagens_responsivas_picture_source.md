
# Imagens Responsivas: `<picture>` e `<source>`

## O que são imagens responsivas?

Imagens responsivas adaptam-se ao tamanho e características da tela do usuário, otimizando o desempenho e a experiência visual. Isso evita o carregamento de imagens muito grandes em dispositivos móveis e melhora a performance.

---

## Elementos principais para imagens responsivas no HTML5

### `<picture>`

- Contêiner que permite usar múltiplas fontes de imagens, selecionadas pelo navegador conforme condições.
- Pode conter vários elementos `<source>` com regras específicas.
- Sempre deve conter uma tag `<img>` como fallback.

### `<source>`

- Define uma fonte de imagem alternativa dentro do `<picture>`.
- Permite definir atributos como `media` e `type` para controlar qual imagem será usada em cada situação.

---

## Estrutura básica

```html
<picture>
  <source media="(min-width: 800px)" srcset="imagem-grande.jpg">
  <source media="(min-width: 400px)" srcset="imagem-media.jpg">
  <img src="imagem-pequena.jpg" alt="Descrição da imagem">
</picture>
```

---

## Como funciona?

- O navegador avalia os elementos `<source>` de cima para baixo.
- Usa o primeiro `<source>` cujo `media` e `type` correspondem às condições atuais.
- Se nenhum `<source>` for adequado, carrega a imagem do `<img>`.

---

## Atributos importantes

| Atributo   | Descrição                                                   |
|------------|-------------------------------------------------------------|
| `media`    | Query CSS que define quando aquela fonte deve ser usada     |
| `srcset`   | URL(s) da imagem(s) que serão carregadas                     |
| `sizes`    | Indica para o navegador a largura da imagem a ser exibida   |
| `type`     | Especifica o tipo MIME da imagem (ex: `image/webp`)          |
| `alt`      | Texto alternativo para acessibilidade                        |

---

## Exemplo avançado com formatos diferentes

```html
<picture>
  <source type="image/webp" srcset="imagem.webp">
  <source type="image/jpeg" srcset="imagem.jpg">
  <img src="imagem.jpg" alt="Descrição da imagem">
</picture>
```

Aqui, o navegador que suporta WebP usará o arquivo `.webp`, que é mais leve.

---

## Dicas para uso eficiente

- Sempre defina o atributo `alt` para acessibilidade.
- Use imagens otimizadas para cada breakpoint para economizar dados.
- Combine `media` e `type` para adaptar imagem a contexto e navegador.
- Teste em vários dispositivos e navegadores.
- Use o atributo `sizes` junto com `srcset` para melhorar a escolha da imagem.

---

## Recursos úteis

- [MDN Web Docs - Elemento `<picture>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture)
- [Responsive Images - HTML Living Standard](https://html.spec.whatwg.org/multipage/images.html#responsive-images)
- [CSS-Tricks - Responsive Images](https://css-tricks.com/responsive-images-youre-just-changing-resolutions-use-srcset/)

---
