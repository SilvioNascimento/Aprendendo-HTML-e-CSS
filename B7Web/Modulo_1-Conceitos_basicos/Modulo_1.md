# Anotações sobre o módulo 1 de B7Web


## Tags:
Uma **tag** em HTML é um elemento básico usado para marcar e estruturar o conteúdo de uma página web. As tags informam ao navegador como o conteúdo deve ser exibido, como textos, imagens, links, tabelas, entre outros.

<hr/>

### Estrutura geral de uma Tag:
Uma tag geralmente é composta por uma _**tag de abertura**_, o _**conteúdo**_ e uma _**tag de fechamento**_:
```
<tag>Conteúdo</tag>
```

#### Componentes:
1. **_Tag de abertura_:**

    * Define o início de um elemento;
    * Exemplo: `<p>` (para um parágrafo).

2. **_Conteúdo_:**

    * O texto, imagem ou outros elementos que a tag deve exibir ou estruturar;
    * Exemplo: "Olá, mundo!" dentro de um parágrafo.

3. **_Tag de fechamento_:**

    * Marca o fim do elemento, precedida por uma barra `/`;
    * Exemplo: `</p>` (fim do parágrafo).

#### Exemplo completo:
```
<p>Olá, mundo!</p>
```
<hr/>

### Tags Sem Conteúdo (Auto-Fechadas):

Algumas tags não têm conteúdo e são auto-fechadas. Elas não precisam de uma tag de fechamento separada.

#### Exemplo:
```
<br />
<hr />
```
<hr/>

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

