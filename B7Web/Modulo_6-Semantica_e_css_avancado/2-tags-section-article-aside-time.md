# Estrutura das Tags HTML: `<section>`, `<article>`, `<aside>` e `<time>`

## O que são?

### `<section>`

A tag `<section>` representa uma seção genérica em um documento, usada para agrupar conteúdos relacionados que formam uma unidade temática. É ideal para dividir o conteúdo em blocos semânticos.

### `<article>`

A tag `<article>` representa um conteúdo independente e autocontido, como um artigo, uma notícia, uma postagem de blog, um comentário ou qualquer bloco que possa ser distribuído ou reutilizado separadamente.

### `<aside>`

A tag `<aside>` é usada para conteúdo que é tangencial ao conteúdo principal, como barras laterais, caixas de informações, links relacionados, anúncios, ou qualquer conteúdo complementar.

### `<time>`

A tag `<time>` representa uma data e/ou hora específica, podendo incluir um valor legível por máquina (`datetime`), o que ajuda na semântica e em mecanismos de busca.

---

## Quando e como usar?

- **`<section>`**  
  Use para dividir o conteúdo em partes temáticas, agrupando elementos relacionados. Cada `<section>` geralmente tem um título (`<h1>` a `<h6>`). Evite usar para apenas estilizar, prefira quando a divisão tem sentido semântico.

- **`<article>`**  
  Use quando o conteúdo for autocontido, que faça sentido isolado. Pode ser um post, notícia, comentário, ou qualquer conteúdo que possa ser distribuído independentemente.

- **`<aside>`**  
  Use para conteúdo que complementa ou está relacionado, mas que não faz parte do fluxo principal. Normalmente barras laterais, citações, listas de links relacionados.

- **`<time>`**  
  Use para marcar datas e horas, como publicações, eventos, prazos. Use o atributo `datetime` para formato padrão ISO legível por máquina.

---

## Exemplos de código

### Exemplo 1: Uso de `<section>` e `<article>`

```html
<section>
  <h2>Notícias Recentes</h2>

  <article>
    <h3>Evento de Tecnologia</h3>
    <p>O evento acontecerá na próxima semana e contará com vários palestrantes.</p>
    <time datetime="2025-06-01">1 de junho de 2025</time>
  </article>

  <article>
    <h3>Lançamento de Produto</h3>
    <p>Nova versão do produto foi lançada com melhorias significativas.</p>
    <time datetime="2025-05-15">15 de maio de 2025</time>
  </article>
</section>
```

### Exemplo 2: Uso de `<aside>` como barra lateral

```html
<aside>
  <h4>Links Relacionados</h4>
  <ul>
    <li><a href="#">Tutorial HTML</a></li>
    <li><a href="#">Guia de CSS</a></li>
    <li><a href="#">JavaScript Básico</a></li>
  </ul>
</aside>
```

### Exemplo 3: Uso do `<time>` com datas e horários

```html
<p>Próximo encontro: <time datetime="2025-05-22T18:30">22 de maio de 2025 às 18:30</time></p>
```
