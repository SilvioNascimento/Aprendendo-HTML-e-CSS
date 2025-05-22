
# Imagens Responsivas: Propriedade `object-fit`

## O que é `object-fit`?

A propriedade CSS `object-fit` define como o conteúdo de um elemento `<img>` ou `<video>` deve ser ajustado dentro da caixa que o contém (container), especialmente quando as proporções do conteúdo e do container são diferentes.

Ela é essencial para controlar o comportamento de imagens em layouts responsivos, evitando distorções e cortes inesperados.

---

## Valores principais

| Valor       | Descrição                                                       |
|-------------|-----------------------------------------------------------------|
| `fill`      | A imagem é esticada para preencher todo o container, podendo distorcer a imagem. |
| `contain`   | A imagem é redimensionada para caber totalmente dentro do container, mantendo proporção. Pode haver espaço vazio. |
| `cover`     | A imagem é redimensionada para cobrir todo o container, mantendo proporção. Pode cortar partes da imagem. |
| `none`      | A imagem mantém seu tamanho original, podendo ultrapassar o container. |
| `scale-down`| A imagem é redimensionada para o menor tamanho entre `none` e `contain`. |

---

## Exemplos práticos

```css
img {
  width: 300px;
  height: 200px;
  object-fit: cover;
}
```

- A imagem preencherá toda a área de 300x200px, cortando partes se necessário para manter a proporção.

---

### Comparação visual

| Valor     | Comportamento                         |
|-----------|-------------------------------------|
| `fill`    | Distorce para preencher o container |
| `contain` | Mantém a imagem toda visível, com espaço sobrando |
| `cover`   | Preenche todo o container, possivelmente cortando imagem |
| `none`    | Mantém tamanho original, pode extrapolar container |
| `scale-down` | Escala para menor entre `none` e `contain`         |

---

## Quando usar `object-fit`?

- Para evitar distorção em imagens responsivas.
- Em galerias de imagens com containers fixos.
- Para criar efeitos de recorte elegante (`cover`).
- Em vídeos responsivos que precisam manter proporção.

---

## Compatibilidade

- Suportado na maioria dos navegadores modernos.
- Internet Explorer não suporta `object-fit` (IE11 tem suporte limitado).

---

## Dicas

- Combine com `overflow: hidden` para garantir que cortes fiquem escondidos.
- Use com imagens `background-image` para mais controle (via `background-size`).
- Teste em vários dispositivos para garantir boa apresentação.

---

## Referências

- [MDN - object-fit](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit)
- [CSS-Tricks - object-fit](https://css-tricks.com/almanac/properties/o/object-fit/)
