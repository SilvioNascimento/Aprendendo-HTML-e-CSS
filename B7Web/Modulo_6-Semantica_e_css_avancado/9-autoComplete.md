# 📝 Anotação HTML: O Atributo `autocomplete`

O atributo **`autocomplete`** é usado em formulários HTML para controlar se o navegador deve ou não preencher automaticamente os campos com base em dados que o usuário inseriu anteriormente. Ele melhora a experiência do usuário, economizando tempo e evitando erros de digitação.

---

## Como Funciona?

Você pode aplicar o `autocomplete` a um formulário inteiro (`<form>`) ou a campos individuais (`<input>`, `<select>`, `<textarea>`).

Os dois valores mais básicos são **"on"** (padrão) e **"off"**.

* **`autocomplete="off"`**: Desliga o preenchimento automático para um campo. É útil para campos sensíveis onde o preenchimento automático pode ser um risco de segurança, como um campo de confirmação de senha ou um código de uso único (token).

    ```html
    <label for="token">Token de Segurança:</label>
    <input type="text" id="token" name="token" autocomplete="off">
    ```

* **`autocomplete="on"`**: Liga explicitamente o preenchimento automático, permitindo que o navegador sugira valores.

    ```html
    <label for="cidade">Sua Cidade:</label>
    <input type="text" id="cidade" name="cidade" autocomplete="on">
    ```

---

### Valores Detalhados para Campos Específicos

A verdadeira força do `autocomplete` está em usar valores mais específicos que dão dicas ao navegador sobre qual tipo de dado o campo espera. Isso permite que o navegador ofereça sugestões muito mais precisas.

#### **Dados Pessoais e de Contato**

* `name`: Nome completo.
* `given-name`: Primeiro nome.
* `family-name`: Sobrenome.
* `email`: Endereço de e-mail.
* `tel`: Número de telefone.
* `address-line1`, `address-line2`: Linhas do endereço.
* `postal-code`: CEP.
* `country-name`: Nome do país.

#### **Exemplo de Endereço:**

```html
<label for="endereco">Endereço:</label>
<input type="text" id="endereco" name="endereco" autocomplete="address-line1">

<label for="cep">CEP:</label>
<input type="text" id="cep" name="cep" autocomplete="postal-code">
```

---

### Gerenciamento de Senhas e Contas 🔒

Usar os valores corretos para login e cadastro é crucial para a integração com gerenciadores de senha dos navegadores.

* `username`: Nome de usuário. Usado em formulários de login.
* `current-password`: Senha atual do usuário. Usado em formulários de login ou para confirmar a identidade antes de uma alteração.
* `new-password`: Nova senha. Usado em formulários de cadastro ou de alteração de senha. O navegador geralmente sugere uma senha forte.

#### Exemplo de Formulário de Login

```html
<form action="/login" method="post">
    <label for="user">Usuário:</label>
    <input type="text" id="user" name="user" autocomplete="username">

    <label for="pass">Senha:</label>
    <input type="password" id="pass" name="pass" autocomplete="current-password">

    <button type="submit">Entrar</button>
</form>
```

#### Exemplo de Formulário de Cadastro

```html
<form action="/cadastro" method="post">
    <label for="novo_user">Escolha um usuário:</label>
    <input type="text" id="novo_user" name="novo_user" autocomplete="username">

    <label for="nova_senha">Crie uma senha:</label>
    <input type="password" id="nova_senha" name="nova_senha" autocomplete="new-password">

    <button type="submit">Cadastrar</button>
</form>
```

Usar `new-password` aciona a funcionalidade do navegador de "Sugerir senha forte", enquanto `current-password` preenche a senha que já está salva para aquele site.
