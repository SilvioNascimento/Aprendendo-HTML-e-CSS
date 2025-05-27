# 📝 Anotação CSS: Degradês (Gradients)

Degradês em CSS permitem criar transições suaves entre duas ou mais cores. Eles não são considerados uma `<color>`, mas sim uma `<image>` (`background-image`), o que os torna extremamente versáteis para preencher o fundo de elementos, criar texturas, sobreposições e muito mais.

Existem três tipos principais de degradês em CSS: **Linear**, **Radial** e **Cônico**.

---

## 1. Degradê Linear (`linear-gradient`)

Este é o tipo mais comum, onde as cores fluem em uma linha reta.

### Sintaxe Básica (Cima para Baixo)

Se você não especificar uma direção, o degradê será aplicado de cima para baixo.

```css
.caixa-linear {
  width: 300px;
  height: 200px;
  /* Sintaxe: linear-gradient(cor-inicial, cor-final) */
  background: linear-gradient(#4c6ef5, #dbe4ff);
}
```

### Controlando a Direção

A direção é o primeiro valor que você pode passar para a função e pode ser definida com palavras-chave ou ângulos.

* **Com palavras-chave:** `to top`, `to right`, `to bottom`, `to left`, `to top right`, etc.
* **Com ângulos:** `45deg`, `90deg`, `180deg`, etc.

#### **Exemplo com direção:**

```css
.caixa-diagonal {
  /* Um degradê que vai do canto inferior esquerdo para o superior direito */
  background: linear-gradient(to top right, #ff9a9e, #fad0c4);
}
```

### Múltiplas Cores e "Color Stops"

Você pode usar quantas cores quiser e controlar exatamente onde a transição de cada cor começa e termina usando "color stops" (paradas de cor).

```css
.faixa-dura {
  /* Criando uma linha dura ao definir a mesma parada para duas cores */
  background: linear-gradient(to right, #364fc7 50%, #c92a2a 50%);
}
```

---

## 2. Degradê Radial (`radial-gradient`)

Neste tipo, as cores se espalham a partir de um ponto central para fora, em formas circulares ou elípticas.

### Sintaxe Básica (Elipse no Centro)

Por padrão, o degradê é uma elipse que começa no centro do elemento.

```css
.caixa-radial {
  width: 300px;
  height: 200px;
  background: radial-gradient(#f76707, #fff4e6);
}
```

### Controlando a Forma e a Posição

Você pode definir a forma (`circle` ou `ellipse`) e a posição do centro do degradê (`at top`, `at left`, `at top right`, etc.).

#### **Exemplo:**

```css
.caixa-posicionada {
  /* Define um círculo que começa no canto superior esquerdo */
  background: radial-gradient(circle at top left, #6741d9, #e5dbff);
}
```

---

## 3. Degradê Cônico (`conic-gradient`)

Este é o tipo mais moderno, onde as cores são distribuídas ao redor de um ponto central, como um gráfico de pizza.

### **Exemplo:**

```css
.grafico-pizza {
  width: 200px;
  height: 200px;
  border-radius: 50%; /* Transforma o elemento em um círculo */
  background: conic-gradient(
    #c92a2a 0deg 90deg,      /* Vermelho de 0 a 90 graus */
    #1864ab 90deg 210deg,     /* Azul de 90 a 210 graus */
    #f59f00 210deg 360deg      /* Laranja de 210 a 360 graus */
  );
}
```

---

## Compatibilidade e "Vendor Prefixes" (Uso Histórico)

Hoje, em **maio de 2025**, a boa notícia é que a sintaxe padrão de `linear-gradient` e `radial-gradient` é suportada por todas as versões modernas dos principais navegadores (Chrome, Firefox, Safari, Edge). **Você raramente precisará usar prefixos**.

No passado, quando essas funcionalidades eram experimentais, cada navegador tinha sua própria versão com um "prefixo de fornecedor" (`vendor prefix`).

* `-webkit-` (Para Chrome, Safari, Opera mais recentes, navegadores de iOS);
* `-moz-` (Para Mozilla Firefox);
* `-o-` (Para Opera mais antigo).

### Exemplo Histórico de Compatibilidade Máxima

Anos atrás, para garantir que um degradê simples de cima para baixo funcionasse em todos os lugares, seu código ficaria assim:

```css
.caixa-compativel {
  /* Para versões antigas do Opera */
  background: -o-linear-gradient(#4c6ef5, #dbe4ff);

  /* Para versões antigas do Firefox */
  background: -moz-linear-gradient(#4c6ef5, #dbe4ff);

  /* Para versões antigas do Chrome e Safari (sintaxe antiga) */
  background: -webkit-linear-gradient(#4c6ef5, #dbe4ff);

  /* A sintaxe padrão (W3C) - a mais importante! Deve vir por último. */
  background: linear-gradient(#4c6ef5, #dbe4ff);
}
```

Note que a sintaxe `-webkit-` antiga também podia usar uma notação diferente para direção (ex: `-webkit-gradient(linear, left top, left bottom, from(#4c6ef5), to(#dbe4ff))`), o que tornava o processo ainda mais complexo.

### Quando Usar os Prefixos Hoje?

**A resposta curta é: quase nunca, pelo menos não manualmente.**

Você só precisaria se preocupar com prefixos para degradês se o seu projeto precisasse dar suporte a navegadores extremamente antigos (lançados antes de 2013-2014), como:

* Safari 6;
* Android Browser 4.3;
* Firefox 15.

Em um fluxo de trabalho moderno, ferramentas de "build" como **Vite** ou **Webpack** usam um **Autoprefixer**. Ele adiciona os prefixos necessários automaticamente com base em uma lista de navegadores que você deseja suportar (`browserslist`), garantindo a compatibilidade sem poluir seu código fonte.

**Conclusão para 2025:** Foque em usar a sintaxe padrão (`linear-gradient`, etc.). Se a compatibilidade com navegadores muito antigos for um requisito, use uma ferramenta com Autoprefixer em vez de escrever os prefixos à mão.

---

## Dicas e Truques Adicionais

### **Degradês Repetidos**

Use repeating-linear-gradient ou repeating-radial-gradient para criar padrões, como listras.

```css
.listrado {
  background: repeating-linear-gradient(
    45deg,
    #364fc7,
    #364fc7 10px,
    #e9ecef 10px,
    #e9ecef 20px
  );
}
```

### **Múltiplos Backgrounds**

Você pode empilhar vários degradês (ou imagens) em um mesmo elemento, separando-os por vírgula. O primeiro da lista fica na camada de cima.

```css
.multi-background {
  background-image:
    linear-gradient(45deg, rgba(255, 255, 255, 0), rgba(255, 255, 255, 0.5)),
    radial-gradient(circle, #1971c2, #6741d9);
}
```
