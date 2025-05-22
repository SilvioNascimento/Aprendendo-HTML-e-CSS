
# Hack CSS: Altura Relativa à Largura para Vídeos Responsivos

## O que é?

Esse hack usa a propriedade `padding-bottom` para fazer com que a altura de um elemento seja proporcional à sua largura, mantendo a proporção original do vídeo (ou outro conteúdo), garantindo responsividade sem distorção.

---

## Por que usar?

- Manter a proporção correta do vídeo em qualquer tamanho de tela.
- Evitar distorções e cortes inesperados.
- Permitir que o vídeo se ajuste a diferentes dispositivos de forma fluida.

---

## Como funciona?

O truque está em usar `padding-bottom` porque, em CSS, o padding vertical é calculado baseado na largura do elemento pai. Assim, definindo um padding em percentual, conseguimos fazer a altura relativa à largura.

---

## Cálculo da porcentagem

Para calcular o valor do `padding-bottom` que mantém a proporção, use a fórmula:

```
padding-bottom = (altura / largura) * 100%
```

### Exemplos

- Proporção 16:9 (Full HD, HD): (9/16) * 100% = 56.25%
- Proporção 4:3: (3/4) * 100% = 75%
- Proporção 21:9 (ultrawide): (9/21) * 100% ≈ 42.86%

---

## Código de exemplo completo baseado no seu código

```html
<div class="video">
  <div class="video-area">
    <iframe
      width="560"
      height="315"
      src="https://www.youtube.com/embed/kk_pGWBOkc4?controls=0"
      frameborder="0"
      allowfullscreen
    ></iframe>
  </div>
</div>
```

```css
.video {
  width: 100%;
  max-width: 800px;
  margin: auto;
}

.video-area {
  position: relative;
  height: 0;
  padding-bottom: 56.25%; /* Proporção 16:9 */
  background-color: #ccc;
}

.video-area iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 0;
}
```

---

## Dicas

- Use `max-width` para limitar o tamanho máximo do vídeo.
- Defina o `position: relative` no container e `position: absolute` no iframe para posicionar corretamente.
- Use a fórmula para calcular o padding-bottom da proporção correta do seu vídeo.
- Alternativamente, em navegadores modernos, utilize a propriedade CSS `aspect-ratio`:

```css
.video-area {
  width: 100%;
  max-width: 800px;
  aspect-ratio: 16 / 9;
}
```

---

## Referências

- [CSS-Tricks: Aspect Ratio Boxes](https://css-tricks.com/aspect-ratio-boxes/)
- [MDN: Padding Percentages](https://developer.mozilla.org/en-US/docs/Web/CSS/padding#percentages)
- [MDN: Aspect Ratio](https://developer.mozilla.org/en-US/docs/Web/CSS/aspect-ratio)

---
