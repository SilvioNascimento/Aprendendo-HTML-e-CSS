# Estilização de Formulários no CSS

Este documento explica as propriedades CSS utilizadas para estilizar os formulários no HTML fornecido.

---

## **1. Reset Global (`box-sizing`)**

```css
* {
    box-sizing: content-box;
}
```

* Define o comportamento do `box-sizing` como `content-box`, garantindo que padding e bordas **não** sejam incluídos no cálculo da largura e altura dos elementos.

---

## **2. Estilização Geral do Corpo (`body`)**

```css
body {
    margin: 50px;
    font-size: 17px;
}
```

* Define uma margem de **50px** em torno da página;
* Define o tamanho da fonte do corpo como **17px**.

---

## **3. Estilização dos Títulos (`h1`)**

```css
h1 {
    font-family: 'Playwrite VN';
}
```

* Define a fonte do título `<h1>` como **'Playwrite VN'**, importada do Google Fonts.

---

## **4. Estilização das Labels (`label`)**

```css
label {
    display: block;
    margin-bottom: 20px;
}
```

* `display: block;` → Faz com que as `<label>` ocupem toda a largura disponível;
* `margin-bottom: 20px;` → Adiciona um espaçamento entre as labels e os campos de entrada.

---

## **5. Estilização dos Campos de Entrada (`input[type=text]`, `textarea`, `select`)**

```css
input[type=text], textarea, select {
    padding: 10px;
    width: 500px;
    font-size: 15px;
    border: 1px solid #CCCCCC;
    outline: 0;
    margin-top: 5px;
}
```

* `padding: 10px;` → Adiciona espaçamento interno para os campos.
* `width: 500px;` → Define a largura fixa de **500px**;
* `font-size: 15px;` → Define o tamanho da fonte dentro dos campos;
* `border: 1px solid #CCCCCC;` → Adiciona uma borda cinza clara ao redor dos campos;
* `outline: 0;` → Remove o contorno ao focar no campo;
* `margin-top: 5px;` → Adiciona um pequeno espaço entre a `<label>` e o campo.

---

## **6. Estilização da Área de Texto (`textarea`)**

```css
textarea {
    height: 200px;
    resize: none;
}
```

* `height: 200px;` → Define a altura do `<textarea>`;
* `resize: none;` → Impede que o usuário redimensione manualmente a área de texto.

---

## **7. Estilização do Link para os Termos (`.termoslink`)**

```css
.termoslink {
    color: black;
    text-decoration: none;
}

.termoslink:hover {
    text-decoration: underline;
}
```

* `.termoslink {}` → Aplica um estilo ao link para os termos de uso;
* `color: black;` → Define a cor do link como preto;
* `text-decoration: none;` → Remove o sublinhado do link;
* `:hover` → Adiciona um sublinhado quando o usuário passa o mouse sobre o link.

---

## **8. Estilização dos Botões (`button`)**

```css
button {
    padding: 10px;
    font-size: 15px;
    border: 1px solid #CCCCCC;
    background-color: #EEEEEE;
}

button:hover {
    background-color: #DDDDDD;
}
```

* `padding: 10px;` → Adiciona espaçamento interno para o botão;
* `font-size: 15px;` → Define o tamanho da fonte do botão;
* `border: 1px solid #CCCCCC;` → Adiciona uma borda cinza clara ao redor do botão;
* `background-color: #EEEEEE;` → Define a cor de fundo padrão do botão;
* `:hover` → Altera a cor de fundo para #DDDDDD quando o usuário passa o mouse sobre o botão.

---

## Resumo da Estilização

* As `<label>` foram estilizadas para ocupar toda a largura e adicionar espaçamento.
* Os campos de entrada (`input`, `textarea`, `select`) foram personalizados com largura fixa, bordas e espaçamento interno.
* O `<textarea>` teve sua altura definida e o redimensionamento desativado.
* Os links para os termos de uso foram estilizados para manter a legibilidade e adicionar um efeito ao passar o mouse.
* Os botões receberam padding, borda, cor de fundo e um efeito `hover`.

Com essas regras CSS, o formulário ficou mais organizado, legível e responsivo para os usuários.
