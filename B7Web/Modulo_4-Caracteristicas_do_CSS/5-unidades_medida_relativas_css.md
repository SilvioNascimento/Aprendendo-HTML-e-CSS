
# Unidades de Medida Relativas no CSS

## O que são unidades relativas?

Unidades relativas são aquelas cujo valor depende de algum outro fator do contexto, como o tamanho da fonte do elemento pai, a raiz do documento, o tamanho da viewport, entre outros. Elas proporcionam flexibilidade e adaptabilidade ao layout, facilitando designs responsivos e acessíveis.

---

## Principais unidades relativas no CSS

| Unidade  | O que representa                                      | Descrição / Uso típico                                                  |
|----------|------------------------------------------------------|------------------------------------------------------------------------|
| `em`     | Multiplicador do tamanho da fonte do elemento pai    | Escala em relação ao tamanho da fonte do elemento pai.                 |
| `rem`    | Multiplicador do tamanho da fonte raiz (`<html>`)    | Escala em relação ao tamanho da fonte raiz da página (normalmente 16px).|
| `%`      | Percentual de uma medida base específica              | Pode variar dependendo da propriedade (ex: largura relativa ao pai).   |
| `vw`     | 1% da largura da viewport (janela de visualização)    | Usado para criar layouts responsivos relacionados à largura da tela.   |
| `vh`     | 1% da altura da viewport                               | Usado para alturas e layouts que dependem da altura da tela.           |
| `vmin`   | O menor valor entre `vw` e `vh`                        | Útil para manter proporções relativas à menor dimensão da viewport.    |
| `vmax`   | O maior valor entre `vw` e `vh`                        | Útil para layouts que precisam considerar a maior dimensão da viewport.|
| `ch`     | Largura do caractere "0" da fonte atual                | Útil para layouts baseados em caracteres, como caixas de texto.        |
| `ex`     | Altura da letra minúscula "x" da fonte atual           | Usada raramente, relacionada à altura x da fonte.                       |

---

## Detalhes e exemplos de uso

### `em`

```css
.parent {
  font-size: 16px;
}
.child {
  font-size: 1.5em; /* 1.5 * 16px = 24px */
}
```

### `rem`

```css
html {
  font-size: 16px;
}
p {
  font-size: 1.25rem; /* 1.25 * 16px = 20px */
}
```

### `%`

```css
.container {
  width: 400px;
}
.box {
  width: 50%; /* 50% de 400px = 200px */
}
```

---

## 🔍 Detalhamento: Unidades Relativas à Viewport

### 📐 O que é viewport?

A **viewport** é a área visível da página no navegador. Seu tamanho muda conforme:

- Tamanho da janela do navegador
- Resolução da tela
- Orientação (retrato ou paisagem)

### 🧮 Unidades de viewport

| Unidade | Significado                          | Descrição prática                              |
|---------|--------------------------------------|------------------------------------------------|
| `1vw`   | 1% da **largura** da viewport        | Se a tela tem 1200px de largura, `1vw = 12px`  |
| `1vh`   | 1% da **altura** da viewport         | Se a tela tem 800px de altura, `1vh = 8px`     |
| `1vmin` | 1% do **menor** entre `vw` e `vh`    | Mantém proporção baseada na menor dimensão     |
| `1vmax` | 1% do **maior** entre `vw` e `vh`    | Mantém proporção baseada na maior dimensão     |

### 📌 Exemplos práticos

```css
header {
  height: 100vh;
}

.banner {
  width: 50vw;
}

.square {
  width: 20vmin;
  height: 20vmin;
}

.full-area {
  width: 90vmax;
}
```

---

## 🔠 Detalhamento das unidades `ch` e `ex`

### `ch` — Largura do caractere "0"

- Representa a largura do caractere "0" da fonte atual.
- Útil para medir largura horizontal de campos de texto ou blocos com base em número de caracteres.

**Exemplo:**

```css
input {
  width: 30ch; /* espaço para 30 caracteres "0" */
}

pre {
  max-width: 80ch; /* ideal para leitura de código */
}
```

**Observações:**

- Em fontes monoespaçadas, `ch` é altamente previsível.
- Em fontes proporcionais, a largura pode variar levemente.

---

### `ex` — Altura da letra "x"

- Representa a altura da letra minúscula “x” (x-height) da fonte atual.
- Útil para ajustes verticais e controle tipográfico preciso.

**Exemplo:**

```css
.icon {
  height: 1ex;
  vertical-align: -0.25ex;
}
```

**Observações:**

- Varia bastante entre fontes diferentes.
- Útil em contextos específicos de tipografia avançada.

---

## Quando usar unidades relativas?

- Para **tipografia fluida**, que se adapta ao contexto ou ao usuário.
- Em **layouts responsivos** para que elementos se ajustem conforme o tamanho da tela.
- Para manter **proporções consistentes** entre elementos.
- Para garantir boa **acessibilidade**.
- Para facilitar o **controle centralizado**, usando `rem`.

---

## Resumo prático para escolha da unidade relativa

| Unidade | Uso recomendado                               |
|---------|----------------------------------------------|
| `em`    | Escalonamento baseado no elemento pai        |
| `rem`   | Escalonamento baseado na raiz do documento   |
| `%`     | Tamanhos relativos ao elemento pai           |
| `vw`, `vh` | Medidas relativas à viewport               |
| `vmin`, `vmax` | Proporções baseadas na viewport       |
| `ch`    | Largura baseada em caracteres                |
| `ex`    | Altura da letra “x”, para ajustes tipográficos |

---
