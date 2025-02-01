# Trabalhando com a Tag `<button>` no HTML

A tag `<button>` é usada para criar botões interativos em páginas da web. Esses botões podem ser usados para enviar formulários, executar scripts JavaScript ou realizar ações no site.

---

## Estrutura básica

A estrutura básica de um botão no HTML é:

```html
<button>Texto do Botão</button>
```

---

## Atributos da Tag `<button>`

### 1. **`type`**

- Define o comportamento do botão.
- Valores disponíveis:
  - `submit`: Envia os dados do formulário ao servidor;
  - `reset`: Limpa todos os campos do formulário;
  - `button`: Não executa nenhuma ação por padrão (usado com JavaScript).
- **Exemplo:**

    ```html
    <button type="submit">Enviar</button>
    ```

### 2. **`name`**

- Define um nome para o botão, útil quando usado em formulários.
- **Exemplo:**

    ```html
    <button type="submit" name="enviar">Enviar</button>
    ```

### 3. **`value`**

- Define um valor associado ao botão quando enviado em um formulário.
- **Exemplo:**

    ```html
    <button type="submit" name="acao" value="cadastrar">Cadastrar</button>
    ```

### 4. **`disabled`**

- Desativa o botão, impedindo cliques e interações.
- **`Exemplo:`**

    ```html
    <button disabled>Indisponível</button>
    ```

### 5. **`autofocus`**

- Define que o botão será focado automaticamente quando a página carregar.
- **Exemplo:**

    ```html
    <button autofocus>Clique Aqui</button>
    ```

### 6. **`form`**

- Associa o botão a um formulário específico pelo `id` do formulário.
- **Exemplo:**

    ```html
    <form id="formulario">
        <input type="text" name="nome">
    </form>
    <button type="submit" form="formulario">Enviar</button>
    ```

### 7. **`formaction`**

- Define a URL para onde os dados do formulário serão enviados (somente para `type="submit"`).
- **Exemplo:**

    ```html
    <button type="submit" formaction="processa.php">Enviar</button>
    ```

---

## Exemplos práticos

### Botão Simples

```html
<button>Clique Aqui</button>
```

### Botão de Envio de Formulário

```html
<form action="cadastro.php" method="post">
    <label for="nome">Nome:</label>
    <input type="text" id="nome" name="nome">
    <button type="submit">Cadastrar</button>
</form>
```

### Botão de Reset do Formulário

```html
<form>
    <input type="text" name="nome">
    <button type="reset">Limpar</button>
</form>
```

### Botão Desativado

```html
<button disabled>Não Clicável</button>
```

### Botão Personalizado com CSS

```html
<style>
    .botao-estilizado {
        background-color: #007BFF;
        color: white;
        padding: 10px 20px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
    }

    .botao-estilizado:hover {
        background-color: #0056b3;
    }
</style>

<button class="botao-estilizado">Botão Estilizado</button>
```

## Considerações Finais

1. **Uso correto do `type`:**
    - Sempre defina `type="button"` para botões que não fazem parte de um formulário, para evitar comportamentos inesperados.

2. **Acessibilidade:**
    - Use botões ao invés de `<div>` ou `<span>` clicáveis, pois eles são mais acessíveis.

3. **Estilização:**
    - Botões podem ser facilmente estilizados com CSS para melhorar a aparência e a experiência do usuário.

---

Com essas informações, você pode criar botões totalmente funcionais e estilizados para interagir melhor com seus usuários no HTML!
