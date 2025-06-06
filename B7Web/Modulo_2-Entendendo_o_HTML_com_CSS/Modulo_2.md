# Anotações sobre o módulo 2 de B7Web

## O que é e como usar o CSS?

### O que é CSS?

CSS (Cascading Style Sheets) é uma linguagem de estilo utilizada para definir a aparência de elementos em páginas web. Ele trabalha junto com o HTML, separando o conteúdo (HTML) da apresentação visual (CSS). Isso facilita a manutenção do site e possibilita criar designs mais sofisticados e responsivos.

### Como usar CSS?

Existem três formas principais de aplicar CSS a um documento HTML:

1. **Inline CSS:**  
   O estilo é aplicado diretamente ao elemento HTML usando o atributo `style`.  

   ```html
   <p style="color: red; font-size: 16px;">Texto vermelho com tamanho de 16px</p>
   ```

2. **CSS Interno (Embedded):**

    O código CSS é inserido dentro de uma tag `<style>` no cabeçalho do documento HTML.

    ```html
    <style>
        h1 {
            color: blue;
            text-align: center;
        }
    </style>
    <h1>Texto centralizado em azul</h1>
    ```

3. **CSS Externo:**

    O estilo está em um arquivo `.css` separado e vinculado ao documento HTML usando a tag `<link>`.

    ```html
    <link rel="stylesheet" href="estilo.css">
    ```

    Conteúdo do arquivo `estilo.css`:

    ```css
    body {
        background-color: #f0f0f0;
        font-family: Arial, sans-serif;
    }
    ```

---

## A base geral do CSS

O CSS utiliza seletores, propriedades e valores para aplicar estilos aos elementos HTML.

### Estrutura básica

```css
seletor {
    propriedade: valor;
}
```

### Seletores

* **Elementos:** Aplica estilo a todos os elementos de um tipo específico.

    Exemplo: `p { color: black; }`

* **Classe:** Usada para estilizar um grupo específico de elementos. Definida com um ponto (`.`).

    ```html
    <div class="caixa"></div>
    ```

    ```css
    .caixa {
        border: 1px solid #ccc;
    }
    ```

* **ID:** Usada para estilizar um único elemento. Definida com o símbolo `#`.

    ```html
    <p id="destaque"></p>
    ```

    ```css
    #destaque {
        font-weight: bold;
    }
    ```

---

## Cores no CSS

### Formas de definir cores

1. **Por nome:**

    ```css
    color: red;
    ```

2. **Código hexadecimal:**

    ```css
    background-color: #00ff00; /* Verde */
    ```

3. **RGB:**

    ```css
    color: rgb(0, 0, 255); /* Azul */
    ```

4. **RGBA:** Igual ao RGB, mas com controle de opacidade.

    ```css
    background-color: rgba(0, 0, 0, 0.5); /* Transparência de 50% */
    ```

5. **HSL:** Hue (matiz), Saturation (saturação) e Lightness (luminosidade).

    ```css
    color: hsl(240, 100%, 50%); /* Azul */
    ```

---

## Bordas no CSS

As bordas no CSS são configuradas com a propriedade `border`, que combina:

1. **Largura:** `1px`, `2em`, etc.
2. **Estilo:** `solid`, `dashed`, `dotted`, etc.
3. **Cor:** `black`, `#333`, etc.

### Tipos de bordas

1. `none`: Remove a borda do elemento.

    ```css
    border: none;
    ```

2. `solid`: Cria uma borda sólida.

    ```css
    border: 2px solid black;
    ```

3. `dashed`: Cria uma borda tracejada.

    ```css
    border: 2px dashed blue;
    ```

4. `dotted`: Cria uma borda pontilhada.

    ```css
    border: 2px dotted green;
    ```

5. `double`: Cria uma borda dupla.

    ```css
    border: 4px double red;
    ```

6. `groove`: Cria uma borda com um efeito de entalhe.

    ```css
    border: 3px groove gray;
    ```

7. `ridge`: Cria uma borda semelhante ao `groove`, mas com o efeito invertido.

    ```css
    border: 3px ridge orange;
    ```

8. `inset`: A borda parece que está "dentro" do elemento.

    ```css
    border: 3px inset purple;
    ```

9. `outset`: A borda parece que está "saindo" do elemento.

    ```css
    border: 3px outset brown;
    ```

10. `hidden`: Oculta a borda, mas mantém o espaço como se ela estivesse presente.

    ```css
    border: hidden;
    ```

### Bordas individuais

Você pode personalizar cada lado da borda separadamente:

```css
div {
    border-top: 2px solid blue;         /* Borda na parte de cima */
    border-right: 2px dotted green;     /* Borda na parte da direita */
    border-bottom: 2px dashed black;    /* Borda na parte de baixo */
    border-left: 2px solid yellow;      /* Borda na parte da esquerda */
}
```

### Bordas arredondadas

A propriedade `border-radius` permite arredondar os cantos de uma borda:

```css
div {
    border: 2px solid black;
    border-radius: 10px; /* Cantos arredondados */
}
```

---

## Margins e Padding no CSS

### O que são **Margin** e **Padding**?

* **Margin:** É o espaço externo ao redor de um elemento HTML, que separa o elemento de outros elementos na página.
* **Padding:** É o espaço interno entre o conteúdo de um elemento e sua borda.

Essas propriedades são essenciais para controlar o espaçamento e posicionamento de elementos em um layout.

---

### Margin

A propriedade `margin` pode ser usada para definir o espaçamento externo de todos os lados de um elemento ou de cada lado separadamente.

#### Propriedades de margem

* **`margin`**: Define a margem de todos os lados de uma só vez.
* **`margin-top`**: Define a margem superior.
* **`margin-right`**: Define a margem direita.
* **`margin-bottom`**: Define a margem inferior.
* **`margin-left`**: Define a margem esquerda.

#### Exemplo de uso

```css
div {
    margin: 20px; /* Aplica 20px de margem em todos os lados */
}
```

#### Exemplo de margens específicas

```css
div {
    margin-top: 10px;      /* Margem superior */
    margin-right: 15px;    /* Margem direita */
    margin-bottom: 5px;    /* Margem inferior */
    margin-left: 20px;     /* Margem esquerda */
}
```

#### Valores possíveis para `margin`

1. **Unidade de medida fixa:** `px`, `em`, `rem`, `%`, etc.

    Exemplo:

    ```css
    margin: 10px; /* Margem de 10 pixels */
    ```

2. **Auto:** Permite centralizar um elemento horizontalmente (usado com `display: block` ou `flex`).

    Exemplo:

    ```css
    div {
        width: 50%;
        margin: 0 auto; /* Centraliza o elemento horizontalmente */
    }
    ```

3. **Herança e valores iniciais:**
    * Valor inicial: `0` (sem margem)
    * `inherit`: Herda o valor da margem do elemento pai.

4. **Shorthand (abreviação):**

    Você pode especificar margens de forma abreviada com até 4 valores:

    ```css
    margin: top right bottom left;
    ```

    Exemplo:

    ```css
    margin: 10px 15px 5px 20px; /* Top: 10px, Right: 15px, Bottom: 5px, Left: 20px */
    ```

### Padding

A propriedade `padding` é usada para definir o espaçamento interno de todos os lados de um elemento ou de cada lado separadamente.

#### Propriedades de padding

* `padding`: Define o preenchimento de todos os lados de uma só vez.
* `padding-top`: Define o preenchimento superior.
* `padding-right`: Define o preenchimento à direita.
* `padding-bottom`: Define o preenchimento inferior.
* `padding-left`: Define o preenchimento à esquerda.

#### Exemplo de uso

```css
div {
    padding: 15px; /* Aplica 15px de preenchimento em todos os lados */
}
```

#### Exemplo de preenchimento específico

```css
div {
    padding-top: 10px;      /* Preenchimento superior */
    padding-right: 20px;    /* Preenchimento à direita */
    padding-bottom: 15px;   /* Preenchimento inferior */
    padding-left: 5px;      /* Preenchimento à esquerda */
}
```

#### Valores possíveis para `padding`

1. **Unidade de medida fixa:** ``px``, ``em``, ``rem``, ``%``, etc.

    Exemplo:

    ```css
    padding: 10px; /* Preenchimento de 10 pixels */
    ```

2. **Porcentagem:** Baseado na largura do elemento pai.

    Exemplo:

    ```css
    padding: 5%; /* Preenchimento de 5% da largura do elemento pai */
    ```

3. **Herança e valores iniciais:**
    * Valor inicial: `0` (sem preenchimento)
    * `inherit`: Herda o valor do preenchimento do elemento pai.

4. **Shorthand (abreviação):** Assim como ``margin``, você pode usar até 4 valores para ``padding``:

    ```css
    padding: top right bottom left;
    ```

    Exemplo:

    ```css
    padding: 10px 15px 5px 20px; /* Top: 10px, Right: 15px, Bottom: 5px, Left: 20px */
    ```

---

### Diferença principais entre **Margin** e **Padding**

| Característica      | Margin                                | Padding                                  |
|---------------------|---------------------------------------|------------------------------------------|
| **Localização**     | Espaço externo ao redor do elemento. | Espaço interno entre conteúdo e borda.  |
| **Afeta o tamanho total** | Não aumenta o tamanho total do elemento. | Aumenta o tamanho total do elemento.     |
| **Uso principal**   | Separar elementos uns dos outros.    | Dar espaçamento interno ao conteúdo.    |

---

### Exemplos combinados de `margin` e `padding`

**Exemplo prático 1:**

```css
div {
    margin: 20px;    /* Espaço externo de 20px */
    padding: 10px;   /* Espaço interno de 10px */
    border: 1px solid black; /* Borda de 1px */
}
```

No exemplo acima, o elemento terá:

* **20px de margem externa**, criando o espaço ao redor;
* **10px de preenchimento interno**, espaçando o conteúdo da borda.

### Exemplo prático 2 (com porcentagens)

```css
div {
    width: 50%;       /* Largura de 50% do elemento pai */
    margin: 10px 5%;  /* Margem: 10px em cima/embaixo e 5% nas laterais */
    padding: 2%;      /* Preenchimento interno de 2% */
}
```

### Exemplo prático 3 (centralização com ``auto``)

```css
div {
    width: 300px;
    margin: 0 auto; /* Centraliza horizontalmente */
    padding: 20px;
    background-color: lightblue;
}
```

Neste caso:

* O elemento será centralizado horizontalmente dentro do pai;
* Haverá 20px de espaço interno.

## Width e Height

As propriedades **`width`** e **`height`** são usadas no CSS para definir a largura e a altura de elementos HTML. Elas são fundamentais no design responsivo e no controle de layout em páginas web.

### Width

A propriedade **`width`** especifica a largura de um elemento. Pode ser definida em valores absolutos, relativos ou utilizando palavras-chave específicas.

#### Valores possíveis

* **Comprimentos absolutos**:
  * Exemplos: `px`, `cm`, `mm`, `in`.
  * Exemplo: `width: 200px;`
* **Percentuais**:
  * Baseados no tamanho do elemento pai.
  * Exemplo: `width: 50%;`
* **Valores automáticos**:
  * O navegador decide a largura com base no conteúdo e no contexto.
  * Exemplo: `width: auto;`
* **Palavras-chave específicas**:
  * Exemplo: `max-content`, `min-content`.

#### Exemplos de uso

```html
<div style="width: 300px; background-color: lightblue;">
  Este elemento tem largura fixa de 300px.
</div>

<div style="width: 50%; background-color: lightcoral;">
  Este elemento ocupa 50% da largura do elemento pai.
</div>
```

### Height

A propriedade **`height`** define a altura de um elemento. Assim como `width`, pode ser especificada em valores absolutos, relativos ou palavras-chave.

#### Valores possíveis

* **Comprimentos absolutos**:
  * Exemplos: `px`, `cm`, `mm`, `in`.
  * Exemplo: `height: 150px;`
* **Percentuais**:
  * Baseados na altura do elemento pai.
  * Exemplo: `height: 100%;`
* **Valores automáticos**:
  * O navegador ajusta a altura com base no conteúdo.
  * Exemplo: `height: auto;`
* **Palavras-chave específicas**:
  * Exemplo: `max-content`, `min-content`.

#### Exemplos de uso

```html
<div style="height: 200px; background-color: lightgreen;">
  Este elemento tem altura fixa de 200px.
</div>

<div style="height: 100%; background-color: lightgoldenrodyellow;">
  Este elemento ocupa 100% da altura do elemento pai.
</div>
```

### Considerações adicionais

* A combinação de `width` e `height` pode ser usada para criar elementos de tamanho fixo ou responsivo.
* As propriedades podem ser combinadas com `max-width`, `min-width`, `max-height` e `min-height` para maior controle.

#### Exemplo prático

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de Width e Height</title>
  <style>
    .box {
      background-color: lightgray;
      border: 1px solid black;
      margin: 10px;
    }
    .fixed {
      width: 200px;
      height: 100px;
    }
    .percentage {
      width: 50%;
      height: 50%;
    }
  </style>
</head>
<body>
  <div class="box fixed">Tamanho fixo: 200px x 100px</div>
  <div class="box percentage">Tamanho relativo: 50% da largura e altura do pai</div>
</body>
</html>
```

Essas propriedades são essenciais para o controle visual e de layout no desenvolvimento de interfaces web. Use-as com sabedoria para alcançar designs elegantes e responsivos!

## Propriedade `box-sizing` no CSS

A propriedade `box-sizing` é usada para alterar o cálculo do tamanho total de um elemento, controlando como a largura e a altura do elemento são calculadas.

---

### **O que é `box-sizing`?**

Por padrão, a largura e a altura de um elemento são determinadas apenas pelo conteúdo, **não incluindo o padding e a borda**. Isso pode dificultar o design de layouts. O `box-sizing` resolve essa questão ao permitir que você altere essa lógica de cálculo.

---

### **Valores de `box-sizing`**

1. **`content-box`** (padrão):  
   O tamanho do elemento inclui apenas o conteúdo. O padding e a borda **não estão incluídos** na largura/altura definidas.

2. **`border-box`**:  
   O tamanho do elemento **inclui o conteúdo, o padding e a borda**. É útil para simplificar o layout, garantindo que o elemento sempre respeite a largura/altura definidas.

---

### **Exemplos**

#### **`content-box` (padrão)**

```html
<div style="width: 200px; padding: 20px; border: 5px solid black; box-sizing: content-box; background-color: lightblue;">
    Este é um exemplo com `content-box`.
</div>
```

* **Largura total** = largura (200px) + padding (20px x 2) + borda (5px x 2) = **250px**
* **Altura total** segue o mesmo cálculo.

---

#### **`border-box`**

```html
<div style="width: 200px; padding: 20px; border: 5px solid black; box-sizing: border-box; background-color: lightgreen;">
    Este é um exemplo com `border-box`.
</div>
```

* **Largura total** = 200px (o valor inclui conteúdo + padding + borda).
* O elemento ocupa exatamente os 200px especificados.

---

### **Usando com CSS global**

É comum usar o valor `border-box` globalmente para simplificar o design.

```css
* {
    box-sizing: border-box;
}
```

Esse código garante que todos os elementos na página usem o cálculo mais intuitivo para largura e altura.

---

### **Comparação prática**

```html
<div style="width: 150px; padding: 10px; border: 3px solid black; box-sizing: content-box; background-color: lightcoral;">
    content-box
</div>

<div style="width: 150px; padding: 10px; border: 3px solid black; box-sizing: border-box; background-color: lightyellow;">
    border-box
</div>
```

#### Resultado

* O elemento com `content-box` será maior porque o padding e a borda são adicionados à largura/altura.
* O elemento com `border-box` terá exatamente 150px, incluindo o padding e a borda.

---

### **Quando usar `box-sizing`?**

* **Layouts responsivos**: Use `border-box` para simplificar o controle do tamanho dos elementos.
* **Elementos com padding**: `border-box` evita surpresas no cálculo do tamanho total.
* **Herdabilidade**: Definir `box-sizing: border-box` globalmente ajuda a manter consistência.

---

## Tag `<a>`

A tag `<a>` em HTML é usada para criar links de navegação, permitindo que o usuário acesse outras páginas, documentos, ou até mesmo partes específicas da mesma página.

---

### **Estrutura básica da tag `<a>`**

A tag `<a>` utiliza o atributo `href` para especificar o destino do link.

#### **Exemplo básico:**

```html
<a href="https://www.example.com">Visite o Example</a>
```

---

### **Atributos Comuns**

1. **`href`**: Especifica o destino do link.
   * Exemplo: `href="https://www.google.com"`

2. **`target`**: Define onde o link será aberto.
   * `_self` (padrão): Abre no mesmo tab.
   * `_blank`: Abre em uma nova aba.
   * Exemplo: `target="_blank"`

3. **`rel`**: Usado com `target="_blank"` para segurança.
   * Exemplo: `rel="noopener noreferrer"`

4. **`title`**: Mostra um texto ao passar o mouse sobre o link.
   * Exemplo: `title="Clique para mais informações"`

---

### **Exemplo Completo:**

```html
<a href="https://www.example.com" target="_blank" rel="noopener noreferrer" title="Visite o Example">
    Clique aqui para visitar o Example
</a>
```

---

### **Personalizando Links com CSS**

Os links podem ser estilizados de forma a mudar a aparência padrão. O CSS permite aplicar estilos em diferentes estados do link.

#### **Pseudo-classes comuns:**

1. **`:link`**: Estiliza links que ainda não foram visitados.
2. **`:visited`**: Estiliza links já visitados.
3. **`:hover`**: Aplica estilo quando o mouse passa sobre o link.
4. **`:active`**: Aplica estilo ao clicar no link.

---

#### **Exemplo de Estilo CSS:**

```html
<style>
  /* Links padrão */
  a {
      color: blue;
      text-decoration: none;
  }

  /* Links visitados */
  a:visited {
      color: purple;
  }

  /* Links ao passar o mouse */
  a:hover {
      color: red;
      text-decoration: underline;
  }

  /* Links durante o clique */
  a:active {
      color: orange;
  }
</style>
```

#### **HTML com estilo aplicado:**

```html
<a href="https://www.example.com">Este é um link estilizado</a>
```

---

### **Estilo Customizado para Botões-Link**

Links podem ser estilizados como botões para melhorar a aparência.

#### **Exemplo de botão-link:**

```html
<style>
  .botao-link {
      display: inline-block;
      background-color: #007BFF;
      color: white;
      padding: 10px 20px;
      text-decoration: none;
      border-radius: 5px;
  }

  .botao-link:hover {
      background-color: #0056b3;
  }
</style>

<a href="https://www.example.com" class="botao-link">Botão-Link</a>
```

---

### **Considerações importantes**

* Sempre use `rel="noopener noreferrer"` ao usar `target="_blank` para segurança.
* Teste os estilos em diferentes navegadores para garantir a consistência.
* Mantenha links acessíveis com textos descritivos que indiquem seu destino.
