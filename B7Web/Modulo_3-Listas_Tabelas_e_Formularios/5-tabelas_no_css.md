
# Tabelas Estilizadas com CSS

O CSS oferece diversas propriedades para estilizar tabelas, tornando-as mais legíveis e visualmente atraentes. Abaixo está uma explicação das propriedades utilizadas em um exemplo de CSS aplicado a tabelas.

---

## **Propriedades CSS para Tabelas**

### 1. **Definindo a largura da tabela**
```css
table {
    width: 600px;
}
```
- Define a largura da tabela como 600 pixels.
- Garante que a tabela tenha um tamanho fixo ou adaptado ao conteúdo.

---

### 2. **Estilizando o cabeçalho (`<thead>`)**
```css
table thead {
    background-color: #CCC;
}
```
- Altera a cor de fundo do cabeçalho da tabela para cinza claro (`#CCC`).

---

### 3. **Estilizando o corpo da tabela (`<tbody>`)**
```css
table tbody {
    background-color: #FFF;
}
```
- Define a cor de fundo padrão do corpo da tabela como branco (`#FFF`).

---

### 4. **Estilizando as células de cabeçalho (`<th>`)**
```css
th {
    font-weight: normal;
}
```
- Remove o negrito padrão dos títulos do cabeçalho (`<th>`).

---

### 5. **Estilizando células (`<th>` e `<td>`)**
```css
th, td {
    padding: 10px;
    text-align: justify;
}
```
- **`padding: 10px;`**: Adiciona espaçamento interno nas células.
- **`text-align: justify;`**: Justifica o texto dentro das células para alinhamento uniforme.

---

### 6. **Efeito ao passar o mouse sobre uma linha**
```css
tbody tr:hover {
    background-color: #EEE;
}
```
- Altera a cor de fundo de uma linha no corpo da tabela (`<tbody>`) para cinza claro (`#EEE`) ao passar o mouse.

---

### 7. **Estilizando linhas pares com `nth-child(even)`**
```css
tbody tr:nth-child(even) {
    background-color: #EEE;
}
```
- Aplica um fundo cinza claro (`#EEE`) às linhas pares do corpo da tabela.
- Facilita a leitura ao alternar as cores das linhas.

---

## **Exemplo Completo de HTML com CSS**

Aqui está a aplicação prática das propriedades acima:

### **HTML**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Estilo de Tabelas com CSS</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Tabela de Produtos</h1>
    <table>
        <thead>
            <tr>
                <th>Produto</th>
                <th>Categoria</th>
                <th>Preço</th>
                <th>Disponibilidade</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Notebook</td>
                <td>Eletrônicos</td>
                <td>R$ 4.500,00</td>
                <td>Em estoque</td>
            </tr>
            <tr>
                <td>Geladeira</td>
                <td>Eletrodomésticos</td>
                <td>R$ 3.200,00</td>
                <td>Fora de estoque</td>
            </tr>
            <tr>
                <td>Fone de Ouvido</td>
                <td>Eletrônicos</td>
                <td>R$ 200,00</td>
                <td>Em estoque</td>
            </tr>
            <tr>
                <td>Smartphone</td>
                <td>Eletrônicos</td>
                <td>R$ 2.800,00</td>
                <td>Em estoque</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

### **CSS**
```css
table {
    width: 600px;
}

table thead {
    background-color: #CCC;
}

table tbody {
    background-color: #FFF;
}

th {
    font-weight: normal;
}

th, td {
    padding: 10px;
    text-align: justify;
}

tbody tr:hover {
    background-color: #EEE;
}

tbody tr:nth-child(even) {
    background-color: #EEE;
}
```

---

## **Resumo das Técnicas**

- **Destaque visual com `hover`**: Realça uma linha quando o mouse passa sobre ela.
- **Melhor leitura com `nth-child(even)`**: Alterna as cores das linhas para facilitar a visualização.
- **Separação visual do cabeçalho (`thead`)**: Cor de fundo distinta para o cabeçalho.

Com essas técnicas, você pode criar tabelas esteticamente agradáveis e fáceis de ler em suas páginas web.
