
# Uso da função CSS `var()` com Media Queries: Exemplo prático

## Definição das variáveis CSS no `:root`

```css
:root {
    --bg-color: #000;
    --bg-second: #444;
    --font-color: #FFF;
    --font-size: 25px;
}
```

Aqui definimos variáveis globais que podem ser usadas em todo o CSS.

---

## Uso das variáveis com `var()`

```css
body {
    background-color: var(--bg-color);
    font-size: var(--font-size);
}

h1, .container {
    color: var(--font-color);
}

.container {
    background-color: var(--bg-second);
}
```

- `body` usa as variáveis para definir a cor de fundo e o tamanho da fonte.
- `h1` e `.container` usam a variável da cor da fonte.
- `.container` também usa variável para cor de fundo secundária.

---

## Alteração dinâmica das variáveis com Media Queries

```css
@media (max-width: 650px) {
    :root {
        --font-size: 18px;
    }
}

@media (max-width: 450px) {
    :root {
        --font-size: 15px;
    }
}
```

- Quando a tela tem no máximo 650px de largura, o tamanho da fonte global (`--font-size`) diminui para `18px`.
- Quando a tela tem no máximo 450px, o tamanho da fonte diminui ainda mais para `15px`.

---

## Como funciona

- As variáveis CSS são definidas globalmente e aplicadas ao corpo e outros elementos.
- Dentro das media queries, redefinimos o valor da variável `--font-size`.
- Isso faz com que todas as propriedades que usam `var(--font-size)` ajustem automaticamente seu valor conforme o tamanho da tela.

---

## Vantagens dessa abordagem

- Centraliza o controle do tamanho da fonte e outras propriedades.
- Facilita a manutenção e alteração de temas e layouts responsivos.
- Evita repetição e garante consistência em todo o CSS.
- O navegador atualiza automaticamente as propriedades que usam a variável quando seu valor muda.

---

## Referência do código completo

```css

/* Função Var */
:root {
    --bg-color: #000;
    --bg-second: #444;
    --font-color: #FFF;
    --font-size: 25px;
}

/* Utilizando variáveis */
body {
    background-color: var(--bg-color);
    font-size: var(--font-size);
}

h1, .container {
    color: var(--font-color);
}

.container {
    background-color: var(--bg-second);
}

@media (max-width: 650px) {
    :root {
        --font-size: 18px;
    }
}

@media (max-width: 450px) {
    :root {
        --font-size: 15px;
    }
}

```

---

## Referências adicionais

- [MDN - Using CSS custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [CSS-Tricks - CSS Variables](https://css-tricks.com/a-complete-guide-to-custom-properties/)
