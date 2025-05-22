
# Tabelas no HTML

As tabelas no HTML são usadas para organizar dados em linhas e colunas. Elas são compostas por várias tags que ajudam a estruturar e estilizar os dados.

---

## **Tags Utilizadas nas Tabelas**

1. **`<table>`**: Define o início e o fim de uma tabela.
   - Exemplo: `<table> ... </table>`

2. **`<tr>`**: Representa uma linha dentro da tabela.
   - Exemplo: `<tr> ... </tr>`

3. **`<th>`**: Define uma célula de cabeçalho (tipicamente na primeira linha ou coluna).
   - Geralmente o texto dentro do `<th>` é exibido em negrito e centralizado.
   - Exemplo: `<th>Nome</th>`

4. **`<td>`**: Define uma célula de dados (as células normais da tabela).
   - Exemplo: `<td>Maria</td>`

5. **`<thead>`**: Agrupa o cabeçalho da tabela. Geralmente contém as tags `<tr>` e `<th>`.
   - Exemplo:

   ```html
   <thead>
       <tr>
           <th>Coluna 1</th>
           <th>Coluna 2</th>
       </tr>
   </thead>
   ```

6. **`<tbody>`**: Agrupa o corpo da tabela, que contém os dados principais.
   - Exemplo:

   ```html
   <tbody>
       <tr>
           <td>Dado 1</td>
           <td>Dado 2</td>
       </tr>
   </tbody>
   ```

7. **`<caption>`** (opcional): Fornece um título descritivo para a tabela.
   - Exemplo: `<caption>Minha Tabela</caption>`

8. **Atributos comuns**:
   - **`border`**: Define a borda da tabela.
   - **`colspan`**: Mescla células horizontalmente (de uma linha).
   - **`rowspan`**: Mescla células verticalmente (de várias linhas).
   - **`width`**: Define a largura da tabela ou de células específicas.
     - Exemplo:

     ```html
     <table width="400">
         <tr>
             <td width="200">Metade da tabela</td>
             <td width="200">Outra metade</td>
         </tr>
     </table>
     ```

---

## **Exemplo de Tabela Completa**

Aqui está um exemplo de uma tabela que organiza os dados fictícios de um time esportivo, com 4 linhas e 6 colunas:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Tabela</title>
</head>
<body>
    <h1>Tabela de Desempenho Esportivo</h1>
    <table width="600" border="1">
        <caption>Desempenho do Time X em Partidas</caption>
        <thead>
            <tr>
                <th>Jogador</th>
                <th>Posição</th>
                <th>Pontos</th>
                <th>Rebotes</th>
                <th>Assistências</th>
                <th>Faltas</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>João</td>
                <td>Armador</td>
                <td>15</td>
                <td>3</td>
                <td>7</td>
                <td>2</td>
            </tr>
            <tr>
                <td>Maria</td>
                <td>Ala</td>
                <td>20</td>
                <td>8</td>
                <td>5</td>
                <td>1</td>
            </tr>
            <tr>
                <td>Lucas</td>
                <td>Pivô</td>
                <td>12</td>
                <td>10</td>
                <td>2</td>
                <td>4</td>
            </tr>
            <tr>
                <td>Ana</td>
                <td>Ala-Armadora</td>
                <td>18</td>
                <td>6</td>
                <td>9</td>
                <td>3</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

---

## **Descrição do Código**

- **Estrutura básica da tabela**:
  - `<table>`: Inicia a tabela e define atributos como `width` e `border`.
  - `<thead>`: Agrupa o cabeçalho, incluindo `<th>` para os títulos.
  - `<tbody>`: Contém os dados principais da tabela usando `<tr>` e `<td>`.

- **Atributos úteis**:
  - **`width`**: Controla a largura da tabela.
  - **`border`**: Adiciona uma borda ao redor da tabela e das células.

---

Com esse exemplo, você pode criar tabelas simples e diretas usando apenas os atributos na tag `<table>` para definir estilo e formatação.
