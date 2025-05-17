# Herança em CSS

A herança em CSS é um mecanismo pelo qual algumas propriedades de estilo aplicadas a um elemento pai são automaticamente aplicadas aos seus elementos filhos. Isso ajuda a manter a consistência visual e evita a repetição desnecessária de regras.

---

## Como Funciona a Herança?

Nem todas as propriedades CSS são herdadas automaticamente. Propriedades relacionadas a texto e fonte geralmente são herdadas, enquanto propriedades relacionadas a layout, caixa e bordas normalmente não.

Por exemplo, se você definir a cor do texto (`color`) no elemento pai, os filhos vão herdar essa cor, a menos que tenham uma cor explicitamente definida.

---

## Propriedades que São Herdadas por Padrão

- `color`
- `font-family`
- `font-size`
- `font-style`
- `font-variant`
- `font-weight`
- `letter-spacing`
- `line-height`
- `list-style`
- `list-style-type`
- `list-style-position`
- `list-style-image`
- `visibility`
- `word-spacing`
- `cursor`
- `quotes`
- `text-indent`
- `text-align`
- `text-transform`
- `text-shadow`
- `white-space`
- `direction`

---

## Propriedades que NÃO São Herdadas por Padrão

- `margin`
- `padding`
- `border`
- `background`
- `width`
- `height`
- `display`
- `position`
- `top`, `left`, `right`, `bottom`
- `float`
- `clear`
- `overflow`
- `box-shadow`
- `z-index`
- Entre outras propriedades relacionadas ao layout e caixa.

---

## Como Forçar a Herança

Você pode forçar a herança de qualquer propriedade usando o valor `inherit`.

Exemplo:

```css
p {
  color: inherit; /* Força a cor a ser herdada do elemento pai */
  border: inherit; /* Força a borda a ser herdada, mesmo não sendo herdada por padrão */
}
```

---

## Como Impedir a Herança

Você pode evitar que uma propriedade seja herdada definindo explicitamente o valor no elemento filho.

Exemplo:

```css
body {
  color: red;
}

p {
  color: black; /* Sobrescreve a cor herdada */
}
```

---

## Exemplo Prático

```html
<style>
  body {
    color: blue;
    font-family: Arial, sans-serif;
  }
  p {
    /* color será herdado como azul */
  }
  span {
    color: inherit; /* força herdar a cor do pai */
  }
  div {
    color: red; /* sobrescreve a herança */
  }
</style>

<body>
  <p>Este texto será azul.</p>
  <div>
    <p>Este texto será vermelho.</p>
    <span>Este texto também será vermelho.</span>
  </div>
</body>
```

---

## Resumo

- A herança em CSS facilita a manutenção do estilo.
- Apenas algumas propriedades são herdadas por padrão.
- Use `inherit` para forçar a herança.
- Sobrescreva valores para impedir herança.
- Conhecer a herança ajuda a escrever CSS mais eficiente e organizado.

---

Compreender a herança em CSS é fundamental para controlar o comportamento visual dos seus elementos e evitar redundâncias no código.
