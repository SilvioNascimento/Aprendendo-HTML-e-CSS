
# Função CSS `var()`

## O que é `var()`?

A função `var()` no CSS é usada para acessar o valor de **variáveis CSS customizadas** (também chamadas de propriedades personalizadas). Elas permitem reutilizar valores de forma dinâmica, facilitando a manutenção e consistência do design.

---

## Estrutura básica

As variáveis CSS são definidas usando a sintaxe:

```css
:root {
  --nome-da-variavel: valor;
}
```

Para usar uma variável, utiliza-se a função:

```css
elemento {
  propriedade: var(--nome-da-variavel);
}
```

---

## Exemplo prático simples

```css
:root {
  --cor-principal: #3498db;
  --padding-base: 16px;
}

.botao {
  background-color: var(--cor-principal);
  padding: var(--padding-base);
  color: white;
  border-radius: 4px;
}
```

Aqui, `.botao` usará a cor e o padding definidos nas variáveis.

---

## Uso de valor padrão (fallback)

Se a variável **não estiver definida**, a função `var()` pode usar um valor padrão para evitar erros:

```css
color: var(--cor-desconhecida, black);
```

Neste caso, se `--cor-desconhecida` não existir, o valor `black` será usado.

---

## Exemplo com fallback

```css
p {
  color: var(--cor-texto, #333333);
}
```

---

## Vantagens das variáveis CSS com `var()`

- **Reutilização:** Defina um valor uma vez e use em vários lugares.
- **Facilidade de manutenção:** Altere a variável que muda todo o design.
- **Dinamismo:** Combine com JavaScript para mudar temas em tempo real.
- **Escopo:** Variáveis podem ser definidas em qualquer seletor e herdam para seus filhos.

---

## Escopo e herança

```css
.container {
  --cor-secundaria: green;
}

.container p {
  color: var(--cor-secundaria);
}
```

Neste exemplo, o parágrafo dentro de `.container` usará o valor da variável definida no container.

---

## Erros comuns e como lidar

- Se você usar uma variável que não foi definida e não fornecer fallback, a propriedade será inválida e ignorada pelo navegador.
- Sempre use um fallback para propriedades importantes, ou defina as variáveis no escopo global (`:root`).
- Variáveis são case-sensitive (`--Cor-Principal` é diferente de `--cor-principal`).

---

## Exemplo completo

```css
:root {
  --cor-fundo: white;
  --cor-texto: black;
}

body {
  background-color: var(--cor-fundo);
  color: var(--cor-texto);
}

button {
  background-color: var(--cor-principal, blue); /* fallback para blue */
  color: var(--cor-texto, white);
  padding: 10px 20px;
}
```

---

## Referências

- [MDN - CSS Custom Properties (variáveis)](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [CSS Tricks - CSS Variables](https://css-tricks.com/a-complete-guide-to-custom-properties/)

---
