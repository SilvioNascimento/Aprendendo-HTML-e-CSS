
# Função CSS `calc()`

## O que é `calc()`?

A função CSS `calc()` permite realizar cálculos matemáticos diretamente dentro das propriedades CSS, combinando unidades diferentes e criando valores dinâmicos e flexíveis.

---

## Sintaxe básica

```css
property: calc(expressão matemática);
```

Exemplo:

```css
width: calc(100% - 50px);
```

---

## Por que usar `calc()`?

- Combinar unidades relativas e absolutas (%, px, em, rem, vw, vh).
- Criar layouts mais flexíveis e responsivos.
- Ajustar tamanhos considerando margens, paddings e outras propriedades.
- Evitar a necessidade de scripts para cálculos simples.

---

## Exemplo baseado no seu código

```css
body {
    margin: 0;
}

.container {
    width: calc(100% - 20px);
    margin: auto;
    height: 200px;
    background-color: #CCC;
}
```

- `width: calc(100% - 20px);` significa que a largura da `.container` será a largura total do seu elemento pai (`100%`), menos 20 pixels.
- `margin: auto;` centraliza a `.container` horizontalmente.
- O `height` está fixado em 200px e a cor de fundo é cinza claro (`#CCC`).

---

## Outros exemplos práticos de `calc()`

### Ajustando largura com padding

```css
.box {
  width: calc(100% - 40px); /* 100% do pai menos 40px de padding */
  padding: 20px;
}
```

### Centralizando verticalmente com altura calculada

```css
.modal {
  height: calc(100vh - 100px); /* Altura da viewport menos 100px */
  margin-top: 50px;
}
```

### Usando múltiplas operações

```css
.element {
  width: calc((100% - 50px) / 3);
}
```

---

## Regras importantes

- Os operadores permitidos são `+`, `-`, `*`, `/`.
- Deve haver espaços entre operadores e valores, por exemplo: `calc(100% - 20px)` (não `calc(100%-20px)`).
- O uso de `calc()` é suportado na maioria dos navegadores modernos.

---

## Vantagens

- Flexibilidade para layouts dinâmicos.
- Reduz complexidade e evita hacks complicados.
- Facilita design responsivo e adaptação a múltiplos dispositivos.

---

## Referências

- [MDN - CSS calc()](https://developer.mozilla.org/en-US/docs/Web/CSS/calc)
- [CSS-Tricks - Using calc() in CSS](https://css-tricks.com/a-couple-of-use-cases-for-css-calc/)

---
