
# Adicionando Fontes Externas no HTML e CSS

A utilização de fontes externas em páginas web permite que você use estilos de texto personalizados além das fontes padrão. Isso é possível utilizando serviços como o **Google Fonts**, ou importando arquivos de fonte diretamente.

---

## **Adicionando Fontes com Google Fonts**

### 1. **Escolhendo uma Fonte**
- Acesse o site do [Google Fonts](https://fonts.google.com).
- Escolha a fonte desejada e clique em "Select preview text" para selecionar os estilos (negrito, itálico, etc.) e para qual linguagem deseja exibir os textos (Portuguese, Abaza, ...).

### 2. **Incorporando no HTML**
Use a tag `<link>` no `<head>` para importar a fonte.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Fonte Externa</title>
    <!-- Importando a fonte Poppins do Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap" rel="stylesheet">
</head>
<body>
    <p style="font-family: 'Poppins', sans-serif;">Este texto usa a fonte Poppins.</p>
</body>
</html>
```

### 3. **Incorporando no CSS**
Você também pode importar a fonte diretamente no CSS usando `@import`.

```css
/* Importando a fonte */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

/* Aplicando a fonte */
body {
    font-family: 'Poppins', sans-serif;
}
```

---

## **Usando Arquivos de Fonte Locais**

### 1. **Passo a Passo**
Se você tem arquivos de fonte (como `.ttf` ou `.woff`), pode hospedá-los localmente no projeto.

- Coloque os arquivos de fonte em uma pasta, por exemplo: `fonts/`.

### 2. **Declarando no CSS**
Use a regra `@font-face` para registrar a fonte.

```css
@font-face {
    font-family: 'MinhaFonte';
    src: url('fonts/minha-fonte.woff2') format('woff2'),
         url('fonts/minha-fonte.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}

/* Aplicando a fonte */
body {
    font-family: 'MinhaFonte', sans-serif;
}
```

---

## **Estratégias para Melhoria de Performance**

1. **Use fontes otimizadas para web**: Arquivos `.woff` e `.woff2` são mais leves que `.ttf` ou `.otf`.
2. **Defina uma fonte padrão (fallback)**: Sempre adicione uma fonte padrão caso a externa não seja carregada.

Exemplo:
```css
body {
    font-family: 'Poppins', Arial, sans-serif;
}
```

3. **Use a opção `display=swap` no Google Fonts**: Isso garante que o texto seja exibido imediatamente com uma fonte padrão até que a fonte externa seja carregada.

---

## **Exemplo Completo**

### Arquivo HTML
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Fontes</title>
    <!-- Importando Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    <!-- Importando CSS -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Usando Fontes Externas</h1>
    <p>Este parágrafo usa a fonte Roboto com peso 400.</p>
</body>
</html>
```

### Arquivo CSS
```css
/* Importando uma fonte local */
@font-face {
    font-family: 'CustomFont';
    src: url('fonts/custom-font.woff2') format('woff2'),
         url('fonts/custom-font.woff') format('woff');
}

/* Aplicando fontes */
body {
    font-family: 'Roboto', 'CustomFont', sans-serif;
}

h1 {
    font-family: 'CustomFont', serif;
}
```

---

Com essas técnicas, você pode criar designs únicos e personalizar textos no seu site de forma eficiente!
