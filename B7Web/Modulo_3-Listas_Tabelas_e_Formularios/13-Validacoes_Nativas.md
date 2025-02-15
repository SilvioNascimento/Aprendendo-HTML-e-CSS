# **Validações Nativas no HTML**

O HTML fornece atributos de validação nativos que ajudam a garantir que os usuários insiram dados corretos nos formulários antes do envio. Esses atributos tornam os formulários mais interativos e evitam a necessidade de validação via JavaScript.

## **1. Atributos de Validação Nativa**

### **1.1 `required`**

* Torna o campo obrigatório, impedindo o envio do formulário se estiver vazio.

* **Exemplo:**

    ```html
    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email" required />
    ```

### **1.2 `maxlength` e `minlength`**

* `maxlength`: Define o número máximo de caracteres que podem ser inseridos;
* `minlength`: Define o número mínimo de caracteres necessários.
* **Exemplo:**

    ```html
    <label for="username">Usuário:</label>
    <input type="text" id="username" name="username" minlength="3" maxlength="15" required />
    ```

### **1.3 `pattern`**

* Define uma **expressão regular** que valida o valor inserido.
* **Exemplo** (Aceita apenas letras minúsculas e números):

    ```html
    <label for="codigo">Código:</label>
    <input type="text" id="codigo" name="codigo" pattern="[a-z0-9]+" title="Somente letras minúsculas e números são permitidos" required />
    ```

### **1.4 `type`**

* Define o tipo de entrada do campo, garantindo validação automática pelo navegador;
* **Valores comuns:**
  * `text` → Texto comum;
  * `email` → Exige um formato válido de e-mail;
  * `url` → Valida se é uma URL válida;
  * `number` → Aceita apenas números;
  * `tel` → Aceita um número de telefone;
  * `password` → Oculta os caracteres;
  * `date` → Exige uma data válida.

* **Exemplo:**

    ```html
    <label for="telefone">Telefone:</label>
    <input type="tel" id="telefone" name="telefone" required />
    ```

### **1.5 `min` e `max`**

* Define **valores mínimo e máximo** para campos do tipo `number` ou `date`.
* **Exemplo** (Número entre 18 e 60):

    ```html
    <label for="idade">Idade:</label>
    <input type="number" id="idade" name="idade" min="18" max="60" required />
    ```

### **1.6 `step`**

* Define **intervalos** de entrada para números e datas.
* **Exemplo** (Aceita apenas múltiplos de 5):

    ```html
    <label for="quantidade">Quantidade:</label>
    <input type="number" id="quantidade" name="quantidade" step="5" required />
    ```

### **1.7 `readonly`**

* Torna o campo **somente leitura**, impedindo alterações.
* **Exemplo:**

    ```html
    <label for="codigo">Código de Usuário:</label>
    <input type="text" id="codigo" name="codigo" value="12345" readonly />
    ```

### **1.8 `disabled`**

* Desabilita o campo, impedindo sua interação.
* **Exemplo:**

    ```html
    <label for="promo">Código Promocional:</label>
    <input type="text" id="promo" name="promo" disabled value="N/A" />
    ```

### **1.9 `autocomplete`**

* Define se o navegador pode sugerir valores previamente inseridos;
* **Valores:**
  * `on` (padrão): → Sugere valores já digitados;
  * `off` → Desativa sugestões automáticas.

* **Exemplo:**

  ```html
  <label for="cidade">Cidade:</label>
  <input type="text" id="cidade" name="cidade" autocomplete="off" />
  ```

### **1.10 `novalidate`**

* Usado na tag `<form>` para **desativar** todas as validações nativas.
* **Exemplo:**

  ```html
  <form action="processa.php" method="post" novalidate>
    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email" required />
    <button type="submit">Enviar</button>
  </form>
  ```

## **2. Exemplo Completo de Formulário com Validações**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário com Validação</title>
</head>
<body>

    <form action="cadastro.php" method="post">

        <label for="nome">Nome:</label>
        <input type="text" id="nome" name="nome" required minlength="3" maxlength="50" />

        <label for="email">E-mail:</label>
        <input type="email" id="email" name="email" required />

        <label for="senha">Senha:</label>
        <input type="password" id="senha" name="senha" required minlength="8" />

        <label for="idade">Idade:</label>
        <input type="number" id="idade" name="idade" min="18" max="99" required />

        <label for="telefone">Telefone:</label>
        <input type="tel" id="telefone" name="telefone" pattern="[0-9]{10,11}" title="Digite um número de telefone válido (10 ou 11 dígitos)" required />

        <label for="website">Site Pessoal:</label>
        <input type="url" id="website" name="website" />

        <button type="submit">Enviar</button>

    </form>

</body>
</html>
```

## **3. Conclusão**

* O HTML permite validações nativas sem necessidade de JavaScript;
* Atributos como `required`, `maxlength`, `pattern` e `type` ajudam a evitar erros de entrada;
* Validar os dados do usuário melhora a experiência e a segurança dos formulários.
