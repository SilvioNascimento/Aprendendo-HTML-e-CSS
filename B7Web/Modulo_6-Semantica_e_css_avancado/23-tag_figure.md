# 📝 Anotação HTML: A Tag `<figure>` e `<figcaption>`

A tag **`<figure>`** é usada para encapsular conteúdo "auto-contido" que é referenciado no fluxo principal do documento, mas que poderia ser movido para outra parte da página (como um apêndice) sem afetar o significado do texto principal. Pense nela como uma forma de agrupar uma ilustração, diagrama, foto, bloco de código, etc., junto com sua legenda.

A tag **`<figcaption>`** é usada (opcionalmente, mas altamente recomendada) para fornecer uma legenda ou título para o conteúdo dentro de um elemento `<figure>`.

---

## O que é a Tag `<figure>`?

- **Propósito:** Marcar conteúdo que é essencialmente independente, mas relevante para o texto ao redor.
- **Tipos de Conteúdo:** Não é apenas para imagens! Você pode usar `<figure>` para agrupar:
  - Imagens (`<img>`)
  - Ilustrações
  - Diagramas
  - Gráficos
  - Blocos de código (`<pre><code>`)
  - Vídeos (`<video>`)
  - Áudios (`<audio>`)
  - Citações (`<blockquote>`)
  - Tabelas (`<table>`)

A ideia central é que, se o conteúdo dentro do `<figure>` fosse removido, o fluxo principal do documento ainda faria sentido, embora uma referência a essa "figura" pudesse ser perdida.

---

## A Legenda com `<figcaption>`

- **Propósito:** Fornecer um título ou uma breve descrição para o conteúdo da `<figure>`.
- **Importância:** Melhora significativamente a acessibilidade, pois leitores de tela podem anunciar a legenda junto com o conteúdo da figura, dando contexto ao usuário.
- **Posicionamento:** A tag `<figcaption>` pode ser o **primeiro** ou o **último** elemento filho dentro de um `<figure>`.

---

## Exemplos Práticos de Uso

### 1. Imagem com Legenda (O Mais Comum)

```html
<figure>
  <img src="imagens/grafico-vendas.png" alt="Gráfico de pizza mostrando o aumento de vendas no último trimestre.">
  <figcaption>Fig. 1 - Crescimento de vendas no último trimestre de 2024.</figcaption>
</figure>
```

No exemplo acima, o texto principal poderia dizer algo como: "... como demonstrado na Figura 1, o crescimento foi notável."

### 2. Bloco de Código com Legenda

`<figure>` é excelente para apresentar exemplos de código de forma semântica.

```html
<figure>
  <figcaption>Exemplo de função JavaScript para saudação:</figcaption>
  <pre><code>function saudar(nome) {
  return `Olá, ${nome}! Bem-vindo(a).`;
}</code></pre>
</figure>
```

### 3. Múltiplas Imagens ou Elementos em uma Única Figura

Uma única `<figure>` pode conter vários elementos visuais que compartilham uma legenda comum.

```html
<figure>
  <img src="produto-vista-frontal.jpg" alt="Produto visto de frente">
  <img src="produto-vista-lateral.jpg" alt="Produto visto de lado">
  <img src="produto-detalhe.jpg" alt="Detalhe do produto">
  <figcaption>Várias vistas do novo Modelo X.</figcaption>
</figure>
```

---

## `<figure>` vs. Atributo `alt` para Imagens (Uma Distinção Importante)

É crucial não confundir a função da `<figcaption>` com o atributo `alt` de uma tag `<img>`.

- **`alt` (Texto Alternativo):** Descreve o *conteúdo visual da imagem* para usuários que não podem vê-la (ex: usuários de leitores de tela ou se a imagem falhar ao carregar). É fundamental para a acessibilidade.
- **`<figcaption>` (Legenda da Figura):** Fornece um título ou uma descrição para a figura como um todo. É visível para todos os usuários e dá contexto à figura dentro do documento.

**Eles são complementares:** Uma imagem dentro de um `<figure>` deve, na maioria das vezes, ter tanto um atributo `alt` descritivo quanto uma `<figcaption>` contextual.

## Conclusão

Usar `<figure>` e `<figcaption>` corretamente enriquece a semântica do seu documento HTML. Isso não apenas ajuda na acessibilidade e no SEO, mas também torna a estrutura do seu conteúdo mais clara e lógica tanto para os navegadores quanto para outros desenvolvedores.

Pense em `<figure>` como uma forma de "enquadrar" e dar destaque a um conteúdo auto-contido e sua legenda.
