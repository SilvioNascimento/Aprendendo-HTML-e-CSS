
# `inherit` no CSS

## 🧾 O que é `inherit`?

A palavra-chave `inherit` no CSS é usada para **forçar a herança de um valor de uma propriedade** do **elemento pai**. Ou seja, mesmo que a propriedade CSS normalmente **não seja herdada automaticamente**, o uso de `inherit` faz com que o valor do elemento pai seja **explicitamente** aplicado ao elemento filho.

---

## 🔍 Como funciona?

Em CSS, algumas propriedades são herdadas por padrão (ex: `color`, `font-family`), enquanto outras não (ex: `margin`, `padding`, `border`). Quando usamos `inherit`, **qualquer propriedade pode herdar o valor de seu pai**, mesmo que normalmente não herdasse.

---

## 📌 Sintaxe

```css
seletor {
  propriedade: inherit;
}
```

---

## ✅ Propriedades com herança natural

Estas **já são herdadas automaticamente** pelos elementos filhos:

- `color`
- `font-family`
- `font-size`
- `line-height`
- `visibility`
- `letter-spacing`
- `word-spacing`
- `text-align`
- `direction`

---

## ❌ Propriedades que NÃO herdam por padrão

- `margin`
- `padding`
- `border`
- `background`
- `width`
- `height`
- `display`
- `position`

Nestes casos, usar `inherit` pode ser útil para **garantir consistência**.

---

## 💡 Exemplos práticos

### Exemplo 1: Herdando `color` explicitamente

```html
<style>
  .parent {
    color: red;
  }

  .child {
    color: inherit;
  }
</style>

<div class="parent">
  Pai
  <div class="child">Filho (herda vermelho)</div>
</div>
```

> Mesmo que `color` seja herdado naturalmente, `inherit` garante o comportamento.

---

### Exemplo 2: Herdando `margin` (que não herda por padrão)

```html
<style>
  .parent {
    margin: 30px;
  }

  .child {
    margin: inherit;
  }
</style>

<div class="parent">
  <div class="child">Filho com mesma margin do pai</div>
</div>
```

---

### Exemplo 3: Estilizando campos de formulário para herdar fontes

```css
input, textarea, select {
  font-family: inherit;
  font-size: inherit;
}
```

> Campos de formulário geralmente **não herdam estilos de fonte** automaticamente. O uso de `inherit` padroniza a aparência.

---

## 🧠 Quando usar `inherit`?

| Situação                                            | Por que usar `inherit`                             |
|-----------------------------------------------------|----------------------------------------------------|
| Garantir consistência entre filhos e o pai          | Força herança em propriedades que não são herdadas |
| Estilizar formulários com aparência consistente     | Form inputs geralmente não herdam fonte nem cor    |
| Criação de temas globais                            | Para adaptar elementos ao estilo global do site    |
| Reset ou normalização de estilos                    | Para garantir previsibilidade em componentes       |

---

## 🚫 Cuidados

- Evite usar `inherit` em cascata sem necessidade, pois pode gerar confusão ou efeitos inesperados.
- Sempre analise se a herança faz sentido sem quebrar o layout.

---

## ✅ Resumo

- `inherit` **força a herança de uma propriedade do pai**.
- Pode ser usado com **qualquer propriedade CSS**.
- Útil para **padronizar layouts**, **formular estilos de inputs** e **evitar repetição**.

---
