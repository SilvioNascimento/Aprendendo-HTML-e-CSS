# Trabalhando com as Tags `<fieldset>` e `<legend>` no HTML

As tags `<fieldset>` e `<legend>` são utilizadas para organizar e agrupar campos dentro de um formulário, tornando-o mais estruturado e acessível.

---

## **1. A Tag `<fieldset>`**

A tag `<fieldset>` é usada para agrupar elementos dentro de um formulário, criando uma separação visual e lógica entre diferentes seções de entrada.

### **Exemplo Básico:**

```html
<fieldset>
    <legend>Informações Pessoais</legend>
    <label>
        Nome: <br/>
        <input type="text" name="nome" />
    </label><br/>
    <label>
        E-mail: <br/>
        <input type="email" name="email" />
    </label><br/>
</fieldset>
```

---

## **2. A Tag `<legend>`**

A tag `<legend>` define um título para o grupo de campos dentro de `<fieldset>`, facilitando a identificação do propósito dos campos agrupados.

### **Exemplo:**

```html
<fieldset>
    <legend>Dados Profissionais</legend>
    <label>
        Empresa: <br/>
        <input type="text" name="empresa" />
    </label><br/>
</fieldset>
```

---

## **3. Estilizando `<fieldset>` e `<legend>` com CSS**

Os estilos CSS podem ser aplicados para melhorar a aparência dos campos agrupados.

### **Exemplo de Código CSS:**

```css
fieldset {
    background-color: #EEE;
    margin-bottom: 20px;
    border: 2px solid #FF0000;
}

legend {
    background-color: #FF0000;
    color: #FFF;
    padding: 5px;
}
```

### **Explicação dos Estilos:**

`fieldset`

* `background-color: #EEE;` → Define uma cor de fundo cinza claro para destacar o grupo de campos;
* `margin-bottom: 20px;` → Adiciona um espaço entre os grupos de campos para uma melhor separação visual;
* `border: 2px solid #FF0000;` → Adiciona uma borda vermelha ao redor do conjunto de campos.

`legend`

* `background-color: #FF0000;` → Define um fundo vermelho para destacar o título do grupo;
* `color: #FFF;` → Define a cor do texto como branca para contraste;
* `padding: 5px;` → Adiciona um preenchimento interno para melhorar a aparência do texto.

---

## **Exemplo Completo de Código HTML e CSS**

### **Código HTML:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página</title>
    <link rel="stylesheet" href="estilo.css">
</head>
<body>
    
    <form method="post">

        <fieldset>
            <legend>Dados Pessoais</legend>
            <label>
                Primeiro nome: <br/>
                <input type="text" name="name" />
            </label><br/>
            <label>
                Sobrenome: <br/>
                <input type="text" name="lastname" />
            </label><br/>
        </fieldset>

        <fieldset>
            <legend>Dados Profissionais</legend>
            <label>
                Nome da empresa: <br/>
                <input type="text" name="companyname" />
            </label><br/>
            <label>
                Cargo da empresa: <br/>
                <input type="text" name="companyjobtitle" />
            </label><br/>
        </fieldset>

        <input type="submit" value="Cadastrar" />

    </form>

</body>
</html>
```

### **Código CSS (`estilo.css`):**

```css
fieldset {
    background-color: #EEE;
    margin-bottom: 20px;
    border: 2px solid #FF0000;
}

legend {
    background-color: #FF0000;
    color: #FFF;
    padding: 5px;
}
```

---

## **Conclusão**

* A tag `<fieldset>` agrupa elementos de um formulário, melhorando a organização.
* A tag `<legend>` adiciona um título ao grupo de campos.
* O CSS pode ser usado para personalizar a aparência e melhorar a experiência do usuário.

Com esse conhecimento, você pode criar formulários mais organizados e visualmente atraentes!
