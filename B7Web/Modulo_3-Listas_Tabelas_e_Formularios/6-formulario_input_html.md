
# Trabalhando com Formulários e Inputs no HTML

Os formulários no HTML são usados para coletar e enviar dados para um servidor ou uma página específica. Eles utilizam diferentes elementos para capturar informações do usuário, como a tag `<input>`.

---

## **1. A Tag `<form>`**

A tag `<form>` define um formulário HTML. Ela serve como contêiner para elementos de entrada como `<input>`, `<textarea>`, `<button>`, entre outros.

### **Principais Atributos**

1. **`action`**:
   - Especifica a URL para onde os dados do formulário serão enviados.
   - Pode ser um caminho relativo ou absoluto.
   - **Exemplo**:
     ```html
     <form action="processa_dados.php">
         <!-- Campos do formulário -->
     </form>
     ```

2. **`method`**:
   - Define o método HTTP usado para enviar os dados.
   - Os valores mais comuns são:
     - **`GET`**: Envia os dados como parte da URL (visíveis).
     - **`POST`**: Envia os dados no corpo da requisição (mais seguro para informações sensíveis).
   - **Exemplo**:
     ```html
     <form action="login.php" method="post">
         <!-- Campos do formulário -->
     </form>
     ```

---

## **Exemplo Completo de Formulário**
```html
<form action="paginas/login.html" method="get">
    <label for="usuario">Usuário:</label>
    <input type="text" id="usuario" name="usuario" />
    <input type="submit" value="Enviar" />
</form>
```
- **`action`**: Envia os dados para a página `login.html`.
- **`method`**: Usa o método `GET` para transmitir os dados.

---

## **2. A Tag `<input>`**

A tag `<input>` é usada para capturar diferentes tipos de entrada do usuário, como texto, senhas, botões, entre outros.

### **Principais Atributos**

1. **`type`**:
   - Define o tipo de entrada. Alguns exemplos comuns:
     - **`text`**: Campo de texto padrão.
     - **`password`**: Campo para senhas (oculta o texto).
     - **`email`**: Campo para e-mail (validação automática em navegadores modernos).
     - **`submit`**: Botão para enviar o formulário.
     - **`button`**: Botão sem funcionalidade associada.
     - **`checkbox`**: Caixa de seleção.
     - **`radio`**: Botão de opção.
     - **`date`**: Seletor de data.
   - **Exemplo**:
     ```html
     <input type="text" name="nome" />
     ```

      Abaixo está a lista completa de tipos de `<input>` com exemplos práticos para cada um:

      #### **`type="text"`**
      - Cria um campo de entrada para texto.
      - **Exemplo**:
        ```html
        <label for="nome">Nome:</label>
        <input type="text" id="nome" name="nome" />
        ```

      ---

      #### **`type="password"`**
      - Cria um campo para entrada de senhas (os caracteres são ocultados).
      - **Exemplo**:
        ```html
        <label for="senha">Senha:</label>
        <input type="password" id="senha" name="senha" />
        ```

      ---

      #### **`type="email"`**
      - Campo para entrada de e-mails (validação automática).
      - **Exemplo**:
        ```html
        <label for="email">E-mail:</label>
        <input type="email" id="email" name="email" />
        ```

      ---

      #### **`type="submit"`**
      - Cria um botão para enviar o formulário.
      - **Exemplo**:
        ```html
        <input type="submit" value="Enviar" />
        ```

      ---

      #### **`type="button"`**
      - Botão simples, sem funcionalidade associada.
      - **Exemplo**:
        ```html
        <input type="button" value="Clique aqui" />
        ```

      ---

      #### **`type="checkbox"`**
      - Cria uma caixa de seleção.
      - **Exemplo**:
        ```html
        <label>
          <input type="checkbox" name="aceito" /> Aceito os termos e condições
        </label>
        ```

      ---

      #### **`type="radio"`**
      - Botão de opção (selecione um entre vários).
      - **Exemplo**:
        ```html
        <label>
          <input type="radio" name="genero" value="masculino" /> Masculino
        </label>
        <label>
          <input type="radio" name="genero" value="feminino" /> Feminino
        </label>
        ```

      ---

      #### **`type="date"`**
      - Cria um seletor de data.
      - **Exemplo**:
        ```html
        <label for="data">Data de nascimento:</label>
        <input type="date" id="data" name="data" />
        ```

      ---

      #### **`type="number"`**
      - Campo para entrada de números.
      - **Exemplo**:
        ```html
        <label for="quantidade">Quantidade:</label>
        <input type="number" id="quantidade" name="quantidade" />
        ```

      ---

      #### **`type="range"`**
      - Cria um controle deslizante.
      - **Exemplo**:
        ```html
        <label for="volume">Volume:</label>
        <input type="range" id="volume" name="volume" min="0" max="100" />
        ```

      ---

      #### **`type="file"`**
      - Cria um seletor de arquivos.
      - **Exemplo**:
        ```html
        <label for="arquivo">Carregar arquivo:</label>
        <input type="file" id="arquivo" name="arquivo" />
        ```

      ---

      #### **`type="color"`**
      - Cria um seletor de cores.
      - **Exemplo**:
        ```html
        <label for="cor">Selecione uma cor:</label>
        <input type="color" id="cor" name="cor" />
        ```

      ---

      #### **`type="tel"`**
      - Campo para entrada de números de telefone.
      - **Exemplo**:
        ```html
        <label for="telefone">Telefone:</label>
        <input type="tel" id="telefone" name="telefone" />
        ```

      ---

      #### **`type="url"`**
      - Campo para entrada de URLs (validação automática).
      - **Exemplo**:
        ```html
        <label for="website">Website:</label>
        <input type="url" id="website" name="website" />
        ```

      ---

2. **`name`**:
   - Identifica o campo de entrada no envio do formulário.
   - O valor deste atributo será enviado junto com os dados do formulário.
   - **Exemplo**:
     ```html
     <input type="email" name="email" />
     ```

3. **`value`**:
   - Define o valor padrão ou o valor associado ao campo de entrada.
   - Para botões (`submit`, `button`), determina o texto exibido.
   - **Exemplo**:
     ```html
     <input type="submit" value="Enviar Formulário" />
     ```

---

## **Exemplo Completo de Inputs**

```html
<form action="cadastro.php" method="post">
    <!-- Campo de texto -->
    <label for="nome">Nome:</label>
    <input type="text" id="nome" name="nome" />

    <!-- Campo de senha -->
    <label for="senha">Senha:</label>
    <input type="password" id="senha" name="senha" />

    <!-- Campo de e-mail -->
    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email" />

    <!-- Botão de envio -->
    <input type="submit" value="Cadastrar" />
</form>
```

---

## **Resumo**
- **`<form>`**:
  - Contém os elementos do formulário.
  - Atributos `action` e `method` controlam o destino e o método de envio.
- **`<input>`**:
  - Captura diferentes tipos de entradas com o atributo `type`.
  - Usa `name` para identificar o campo e `value` para valores padrão.

Com essas informações, você pode criar formulários robustos e interativos no HTML.
