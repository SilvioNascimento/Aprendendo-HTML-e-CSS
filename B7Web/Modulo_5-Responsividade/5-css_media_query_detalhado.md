
# CSS `@media` Queries

## O que são `@media` queries?

`@media` queries são uma funcionalidade essencial do CSS que permite aplicar estilos diferentes dependendo das **características da tela** ou do dispositivo, como tamanho, resolução, orientação e muito mais. Elas são fundamentais para criar **layouts responsivos**, permitindo que um site ou aplicação se adapte a diferentes tamanhos de tela e dispositivos.

---

## Sintaxe básica

A sintaxe básica para `@media` queries é:

```css
@media (condição) {
  /* Regras de estilo */
}
```

### Exemplo simples

```css
@media (min-width: 768px) {
  body {
    background-color: lightblue;
  }
}
```

> Neste exemplo, o fundo da página será `lightblue` apenas em telas com largura mínima de 768px.

---

## Tipos de `@media` queries

### Condições comumente usadas

- `min-width`: Largura mínima da viewport (tela).
- `max-width`: Largura máxima da viewport.
- `min-height`: Altura mínima da viewport.
- `max-height`: Altura máxima da viewport.
- `orientation`: A orientação da tela (retrato ou paisagem).
- `resolution`: Resolução da tela (ex: alta resolução em dispositivos móveis).
- `aspect-ratio`: A proporção entre largura e altura da tela.

### Exemplo de múltiplas condições

```css
@media (min-width: 600px) and (max-width: 1024px) {
  .container {
    padding: 20px;
  }
}
```

> Este código aplica um padding de 20px apenas em telas entre 600px e 1024px.

---

## Variação com `orientation`

### ✅ O que é `orientation`?

A propriedade `orientation` permite que você aplique estilos com base na **orientação da tela**, ou seja, se a tela está **em modo retrato (portrait)** ou **paisagem (landscape)**.

- **Portrait**: Quando a altura da tela é maior que a largura (geralmente em dispositivos móveis quando segurados de forma vertical).
- **Landscape**: Quando a largura da tela é maior que a altura (geralmente em dispositivos móveis quando segurados de forma horizontal ou em telas grandes).

### 📌 Exemplos de uso

```css
@media (orientation: portrait) {
  body {
    background-color: lightblue;
  }
}

@media (orientation: landscape) {
  body {
    background-color: lightgreen;
  }
}
```

> Neste exemplo, o fundo da página muda dependendo da orientação da tela.

---

## 📏 `aspect-ratio` em `@media`

### ✅ O que é `aspect-ratio`?

A propriedade `aspect-ratio` em `@media` queries permite definir **condições baseadas na proporção entre a largura e a altura** da tela ou de um elemento.

### 📌 Sintaxe

```css
@media (aspect-ratio: <largura>/<altura>) {
  /* Estilos para quando a proporção for <largura>/<altura> */
}

@media (min-aspect-ratio: 4/3) {
  /* Estilos para telas com uma proporção maior ou igual a 4:3 */
}
```

### 📌 Exemplos de uso

#### Exemplo 1: Mudando a disposição de elementos com base na proporção da tela

```css
@media (aspect-ratio: 16/9) {
  .content {
    height: 60vh;
  }
}

@media (aspect-ratio: 4/3) {
  .content {
    height: 50vh;
  }
}
```

> Aqui, o conteúdo terá uma altura diferente dependendo da proporção da tela.

#### Exemplo 2: Utilizando `min-aspect-ratio`

```css
@media (min-aspect-ratio: 16/9) {
  .video-player {
    width: 100%;
    height: auto;
  }
}

@media (max-aspect-ratio: 4/3) {
  .video-player {
    width: 100%;
    height: 100%;
  }
}
```

> Aqui, o estilo para o player de vídeo muda dependendo da proporção da tela. Para telas com proporção mínima de 16:9, o player ajusta sua altura automaticamente. Para telas com uma proporção máxima de 4:3, ele ocupa 100% da altura e largura do container.

---

## Dicas para usar `@media` queries

1. **Mobile First**: Comece criando o design para dispositivos móveis (uso de `min-width`).
2. **Evite múltiplas consultas desnecessárias**: Combine condições quando possível.
3. **Desempenho**: Teste em vários dispositivos para garantir que as mudanças de layout não impactem o desempenho.

---

## Exemplo de `@media` query para imagens responsivas

```css
@media (max-width: 768px) {
  .hero-image {
    background-image: url('mobile-image.jpg');
  }
}

@media (min-width: 769px) {
  .hero-image {
    background-image: url('desktop-image.jpg');
  }
}
```

> Neste exemplo, o fundo da imagem será alterado dependendo do tamanho da tela, otimizando a performance.

---

## Recursos úteis

- [MDN - @media](https://developer.mozilla.org/en-US/docs/Web/CSS/@media)
- [CSS-Tricks - Media Queries](https://css-tricks.com/css-media-queries/)
- [W3Schools - CSS Media Queries](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)

---
