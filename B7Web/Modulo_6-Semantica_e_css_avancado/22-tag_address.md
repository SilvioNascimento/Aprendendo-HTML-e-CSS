# 📝 Anotação HTML: A Tag `<address>`

A tag **`<address>`** em HTML tem um propósito semântico muito específico: fornecer **informações de contato** para o autor ou proprietário do seu documento ou de um artigo (`<article>`) específico.

Ela não deve ser usada para marcar qualquer endereço postal aleatório em uma página. A informação dentro da `<address>` deve ser sobre o contato da pessoa ou organização responsável pelo conteúdo.

## O que colocar dentro da `<address>`?

As informações podem incluir:

- Nome do autor ou da organização.
- Um link para um site.
- Um link de e-mail (usando `mailto:`).
- Um endereço físico.
- Um número de telefone.
- Links para redes sociais.

**Aparência Padrão:** Por padrão, os navegadores renderizam o texto dentro da tag `<address>` em itálico, mas isso pode ser facilmente alterado com CSS (`font-style: normal;`).

---

## Como e Onde Usar `<address>`

A tag `<address>` pode ser usada em dois contextos principais:

### 1. Contato do Site Inteiro (Dentro do `<footer>`)

Este é o uso mais comum. Quando colocada no rodapé do site, a tag `<address>` fornece as informações de contato para o proprietário do site ou da página inteira.

**Exemplo:**

```html
<footer>
  <address>
    <p>Desenvolvido por Maria da Silva.</p>
    <p>Entre em contato: <a href="mailto:contato@meusite.com">contato@meusite.com</a></p>
    <p>Visite-nos em Guarabira, PB.</p>
  </address>
</footer>
```

### 2. Contato do Autor de um Artigo (Dentro de `<article>`)

Quando usada dentro de um elemento `<article>`, a tag `<address>` se refere especificamente ao autor daquele artigo, e não ao site como um todo.

**Exemplo:**

```html
<article>
  <h2>Como Fazer Café na Paraíba</h2>
  <p>O café é uma paixão regional...</p>
  
  <footer>
    <address>
      <p>Postado por João Pereira</p>
      <p>Siga-o no Twitter: <a href="https://twitter.com/joaopereiradev">@joaopereiradev</a></p>
    </address>
  </footer>
</article>
```

---

## O que NÃO fazer com `<address>`

O erro mais comum é usar a tag `<address>` para marcar um endereço postal que **não** é a informação de contato do autor/dono do conteúdo.

- ❌ **JEITO ERRADO:** Se você está escrevendo um artigo sobre a localização da prefeitura de Guarabira.

    ```html
    <p>A prefeitura fica no seguinte endereço:</p>
    <address>
    Rua Solon de Lucena, 26, Centro, Guarabira - PB, 58200-000
    </address>
    ```

- ✅ **JEITO CERTO:** Para marcar um endereço arbitrário, use apenas um parágrafo `<p>` ou outra tag apropriada.

    ```html
    <p>A prefeitura fica no seguinte endereço:</p>
    <p>Rua Solon de Lucena, 26, Centro, Guarabira - PB, 58200-000</p>
    ```

## Conclusão

Use a tag `<address>` para dar significado semântico às informações de contato do criador do conteúdo. Isso ajuda os navegadores e os mecanismos de busca a entenderem quem é o responsável por aquele documento ou artigo, melhorando a estrutura e a acessibilidade da sua página.
