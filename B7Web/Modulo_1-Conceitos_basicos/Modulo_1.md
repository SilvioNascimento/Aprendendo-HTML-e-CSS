# Anotações sobre o módulo 1 de B7Web

## Tags

Uma **tag** em HTML é um elemento básico usado para marcar e estruturar o conteúdo de uma página web. As tags informam ao navegador como o conteúdo deve ser exibido, como textos, imagens, links, tabelas, entre outros.

---

### Estrutura geral de uma Tag

Uma tag geralmente é composta por uma _**tag de abertura**_, o _**conteúdo**_ e uma _**tag de fechamento**_:

```html
<tag>Conteúdo</tag>
```

#### Componentes

1. **_Tag de abertura_:**

    * Define o início de um elemento;
    * Exemplo: `<p>` (para um parágrafo).

2. **_Conteúdo_:**

    * O texto, imagem ou outros elementos que a tag deve exibir ou estruturar;
    * Exemplo: "Olá, mundo!" dentro de um parágrafo.

3. **_Tag de fechamento_:**

    * Marca o fim do elemento, precedida por uma barra `/`;
    * Exemplo: `</p>` (fim do parágrafo).

#### Exemplo completo

```html
<p>Olá, mundo!</p>
```

---

### Tags Sem Conteúdo (Auto-Fechadas)

Algumas tags não têm conteúdo e são auto-fechadas. Elas não precisam de uma tag de fechamento separada.

#### Exemplo

```html
<br />
<hr />
```

---

### Tabela em HTML

A tabela a seguir informa sobre as tags HTML, suas descrições e suas estruturas. Vale informar que a maioria das informações da tabela foram obtidas através da ajuda da inteligência artificial **ChatGpt**.

###

| **Tag HTML**      | **Descrição**                                                                 | **Estrutura**                              |
|--------------------|-------------------------------------------------------------------------------|--------------------------------------------|
| `<html>`          | Define o documento HTML.                                                     | `<html> ... </html>`                       |
| `<head>`          | Contém metadados do documento, como título e links para estilos ou scripts.  | `<head> ... </head>`                       |
| `<title>`         | Define o título da página, exibido na aba do navegador.                      | `<title>Meu Título</title>`                |
| `<body>`          | Contém o conteúdo visível do documento.                                      | `<body> ... </body>`                       |
| `<h1>` a `<h6>`   | Títulos de diferentes níveis (de maior para menor importância).              | `<h1>Título</h1>`                          |
| `<p>`             | Define um parágrafo de texto.                                                | `<p>Texto do parágrafo</p>`                |
| `<a>`             | Define um link para outra página ou recurso.                                 | `<a href="URL">Texto do link</a>`          |
| `<img>`           | Insere uma imagem.                                                          | `<img src="URL" alt="Descrição" />`        |
| `<ul>`            | Cria uma lista não ordenada (com marcadores).                                | `<ul> ... </ul>`                           |
| `<ol>`            | Cria uma lista ordenada (numerada).                                          | `<ol> ... </ol>`                           |
| `<li>`            | Define um item em uma lista (`<ul>` ou `<ol>`).                              | `<li>Item da lista</li>`                   |
| `<div>`           | Define uma divisão ou seção no documento.                                    | `<div> ... </div>`                         |
| `<span>`          | Define uma parte específica de texto ou inline dentro de outro conteúdo.     | `<span>Texto</span>`                       |
| `<table>`         | Cria uma tabela.                                                            | `<table> ... </table>`                     |
| `<tr>`            | Define uma linha em uma tabela.                                              | `<tr> ... </tr>`                           |
| `<td>`            | Define uma célula de dados em uma linha da tabela.                           | `<td>Conteúdo</td>`                        |
| `<th>`            | Define uma célula de cabeçalho em uma tabela.                                | `<th>Cabeçalho</th>`                       |
| `<form>`          | Cria um formulário para entrada de dados.                                    | `<form action="URL" method="GET/POST">...</form>` |
| `<input>`         | Define um campo de entrada no formulário.                                    | `<input type="text" name="campo" />`       |
| `<button>`        | Cria um botão clicável.                                                      | `<button>Texto do botão</button>`          |
| `<br>`            | Insere uma quebra de linha.                                                  | `<br />`                                   |
| `<hr>`            | Insere uma linha horizontal para separar conteúdos.                         | `<hr />`                                   |
| `<strong>`        | Define texto com ênfase forte (geralmente em negrito).                       | `<strong>Texto</strong>`                   |
| `<em>`            | Define texto enfatizado (geralmente em itálico).                             | `<em>Texto</em>`                           |

---

## Atributos

Os **atributos em HTML** são usados para fornecer informações adicionais sobre os elementos. Eles são sempre especificados na **_tag de abertura_** e vêm no formato **_nome=valor_**.

---

### Estrutura Geral de um Atributo

```html
<tag atributo="valor">Conteúdo</tag>
```

---

### Exemplos de Atributos Comuns

1. `id`

    Identifica um elemento de forma única na página.

    ```html
    <div id="cabecalho">Bem-vindo!</div>
    ```

2. `class`

    Define uma ou mais classes para estilizar ou selecionar elementos com CSS e JavaScript.

    ```html
    <p class="texto-destaque">Texto em destaque.</p>
    ```

3. `src`

    Especifica a URL de um recurso externo, como imagens ou scripts.

    ```html
    <img src="imagem.jpg" alt="Descrição da imagem" />
    ```

4. `href`

    Especifica o destino de um link.

    ```html
    <a href="https://www.example.com">Visite o site</a>
    ```

5. `alt`

    Fornece uma descrição alternativa para imagens (usado para acessibilidade e quando a imagem não pode ser carregada).

    ```html
    <img src="logo.png" alt="Logo da empresa" />
    ```

6. `title`

    Adiciona uma descrição que aparece como dica (tooltip) ao passar o mouse sobre o elemento.

    ```html
    <button title="Clique aqui para enviar">Enviar</button>
    ```

7. `style`

    Define estilos diretamente em um elemento.

    ```html
    <h1 style="color: blue; font-size: 20px;">Título Azul</h1>
    ```

8. `type`

    Define o tipo de um elemento (geralmente usado em `<input>` ou `<button>`).

    ```html
    <input type="text" placeholder="Digite seu nome" />
    ```

9. `placeholder`

    Define um texto de sugestão em campos de entrada.

    ```html
    <input type="email" placeholder="Digite seu e-mail" />
    ```

---

10. `value`

    Define um valor padrão para elementos como `<input>` ou `<textarea>`.

    ```html
    <input type="text" value="Preenchido automaticamente" />
    ```
