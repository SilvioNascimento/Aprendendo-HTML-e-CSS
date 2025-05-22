
# Funções CSS `min()` e `max()` com Exemplos Práticos

## O que são?

As funções CSS `min()` e `max()` permitem definir valores dinâmicos escolhendo automaticamente o menor (`min()`) ou maior (`max()`) valor dentre os argumentos fornecidos.

---

## Exemplo de uso com código

```css
/* Utilizando o max() */
img {
    width: max(50%, 300px);
}

/* Utilizando o min() */
img {
    width: min(50%, 300px);
}
```

---

## Como funciona o exemplo?

- `width: max(50%, 300px);`
  - A largura da imagem será o **maior valor** entre 50% da largura do contêiner pai e 300 pixels.
  - Isso significa que a imagem terá no mínimo 300px de largura, podendo ser maior se 50% do container for maior que 300px.

- `width: min(50%, 300px);`
  - A largura da imagem será o **menor valor** entre 50% da largura do contêiner pai e 300 pixels.
  - A imagem terá no máximo 300px de largura, podendo ser menor se 50% do container for menor que 300px.

---

## Dicas para uso

- Use `max()` para garantir um tamanho **mínimo** que não será ultrapassado para mais baixo.
- Use `min()` para garantir um tamanho **máximo** que não será ultrapassado para mais alto.
- Combine com unidades relativas (`%`, `vw`, `vh`) e absolutas (`px`) para flexibilidade.
- Ideal para tornar elementos responsivos mantendo limites mínimos e máximos.

---

## Outras aplicações comuns

- Definir tamanhos mínimos e máximos de fontes, caixas, imagens e botões.
- Controlar larguras e alturas para melhor adaptabilidade em layouts responsivos.
- Evitar que elementos fiquem muito pequenos ou muito grandes em telas diferentes.

---

## Referências

- [MDN - CSS min()](https://developer.mozilla.org/en-US/docs/Web/CSS/min)
- [MDN - CSS max()](https://developer.mozilla.org/en-US/docs/Web/CSS/max)
- [CSS-Tricks - min(), max() and clamp()](https://css-tricks.com/a-guide-to-the-css-min-max-and-clamp-functions/)

---
