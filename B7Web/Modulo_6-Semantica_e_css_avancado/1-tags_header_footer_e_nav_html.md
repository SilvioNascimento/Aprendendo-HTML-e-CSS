# Estrutura das Tags HTML: `<header>`, `<footer>` e `<nav>`

## O que são?

### `<header>`

A tag `<header>` representa um contêiner para conteúdo introdutório ou um conjunto de links de navegação. Geralmente contém o título da página, logo, menu principal, ou elementos introdutórios.

### `<footer>`

A tag `<footer>` define um rodapé para o seu documento ou seção. Normalmente contém informações sobre o autor, direitos autorais, links importantes, informações de contato, entre outros.

### `<nav>`

A tag `<nav>` é usada para definir uma seção de navegação que contém links para outras partes do site ou para páginas externas. Geralmente é usada para menus principais, barras laterais ou rodapés com links.

---

## Quando usar?

- **`<header>`**  
  Use quando precisar de uma área de introdução ao conteúdo ou uma seção que inclua título, logotipo, slogan, ou menus principais. Pode ser usado tanto no `<body>` para o cabeçalho geral da página, quanto dentro de outras seções para cabeçalhos locais.

- **`<footer>`**  
  Use para definir o rodapé da página ou de uma seção específica. Normalmente contém informações de contato, copyright, links importantes ou outras informações complementares.

- **`<nav>`**  
  Use para agrupar links de navegação principais da página ou de uma seção específica. Ajuda na acessibilidade e no entendimento da estrutura do site por motores de busca.

---

## Dicas

- Sempre que possível, use essas tags semânticas para melhorar a estrutura do HTML e a acessibilidade.
- Evite usar `<nav>` para pequenos grupos de links, como links de redes sociais; para isso, pode ser melhor usar listas simples ou `<div>`.
- Você pode ter múltiplos `<header>`, `<footer>` e `<nav>` em uma página, desde que sejam para seções diferentes.
- Use o `<nav>` para menus principais e secundários que realmente sejam de navegação.
- Dentro do `<header>` e `<footer>`, é comum ter elementos como `<h1>`, `<p>`, `<ul>`, e `<nav>`.

---

## Exemplos de Código

### Exemplo 1: Estrutura básica com `<header>`, `<nav>` e `<footer>`

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <title>Exemplo de Estrutura Semântica</title>
</head>
<body>
  <header>
    <h1>Meu Site</h1>
    <nav>
      <ul>
        <li><a href="#home">Início</a></li>
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section id="home">
      <h2>Bem-vindo ao meu site</h2>
      <p>Conteúdo da página inicial.</p>
    </section>
    <section id="sobre">
      <h2>Sobre Nós</h2>
      <p>Informações sobre a empresa.</p>
    </section>
  </main>

  <footer>
    <p>© 2025 Meu Site. Todos os direitos reservados.</p>
  </footer>
</body>
</html>
```

---

### Exemplo 2: Cabeçalho e rodapé em uma seção específica

```html
<section>
  <header>
    <h2>Artigo Importante</h2>
    <p>Autor: João Silva</p>
  </header>

  <article>
    <p>Conteúdo do artigo aqui...</p>
  </article>

  <footer>
    <p>Publicado em 22 de maio de 2025</p>
  </footer>
</section>
```
