
# Trabalhando com a Tag `<textarea>` no HTML

A tag `<textarea>` é usada para criar campos de texto multilinha em formulários, permitindo que os usuários insiram grandes quantidades de texto, como comentários, descrições ou mensagens.

---

## **Estrutura Básica**

A estrutura básica da tag `<textarea>` é a seguinte:

```html
<textarea></textarea>
```

---

## **Atributos da Tag `<textarea>`**

### 1. **`name`**

- Define o nome do campo para envio dos dados no formulário.
- **Exemplo**:

  ```html
  <textarea name="comentario"></textarea>
  ```

### 2. **`id`**

- Identifica o elemento para vinculá-lo a um rótulo `<label>`.
- **Exemplo**:

  ```html
  <label for="mensagem">Mensagem:</label>
  <textarea id="mensagem" name="mensagem"></textarea>
  ```

### 3. **`rows`** (Não recomendado)

- Especifica o número de linhas visíveis no campo.
- **Exemplo**:

  ```html
  <textarea name="descricao" rows="5"></textarea>
  ```

### 4. **`cols`** (Não recomendado)

- Define a largura do campo em número de caracteres.
- **Exemplo**:

  ```html
  <textarea name="descricao" cols="50"></textarea>
  ```

### 5. **`placeholder`**

- Exibe um texto dentro do campo como uma dica ao usuário, que desaparece quando o campo é preenchido.
- **Exemplo**:

  ```html
  <textarea placeholder="Digite seu comentário aqui"></textarea>
  ```

### 6. **`maxlength`**

- Limita o número máximo de caracteres que podem ser digitados.
- **Exemplo**:

  ```html
  <textarea maxlength="200"></textarea>
  ```

### 7. **`readonly`**

- Torna o campo somente leitura, ou seja, impede que o usuário edite o texto.
- **Exemplo**:

  ```html
  <textarea readonly>Este campo é somente leitura.</textarea>
  ```

### 8. **`disabled`**

- Desativa o campo, impedindo que ele seja usado.
- **Exemplo**:

  ```html
  <textarea disabled>Este campo está desativado.</textarea>
  ```

### 9. **`required`**

- Indica que o preenchimento do campo é obrigatório antes do envio do formulário.
- **Exemplo**:

  ```html
  <textarea name="comentario" required></textarea>
  ```

---

## **Exemplos Práticos**

### **Campo Simples**

```html
<label for="comentario">Deixe seu comentário:</label>
<textarea id="comentario" name="comentario"></textarea>
```

---

### **Campo com Placeholder**

```html
<label for="descricao">Descrição:</label>
<textarea id="descricao" name="descricao" placeholder="Digite uma breve descrição"></textarea>
```

---

### **Campo com Tamanho Personalizado**

```html
<label for="mensagem">Mensagem:</label>
<textarea id="mensagem" name="mensagem" rows="4" cols="50"></textarea>
```

---

### **Campo com Limite de Caracteres**

```html
<label for="feedback">Feedback (máximo 200 caracteres):</label>
<textarea id="feedback" name="feedback" maxlength="200"></textarea>
```

---

### **Campo Somente Leitura**

```html
<label for="info">Informação:</label>
<textarea id="info" name="info" readonly>Este é um texto fixo que não pode ser editado.</textarea>
```

---

### **Campo Desativado**

```html
<label for="nota">Nota:</label>
<textarea id="nota" name="nota" disabled>Este campo está desativado.</textarea>
```

---

## **Dicas de Uso**

1. **Acessibilidade**:
   - Use o atributo `label` para descrever o campo e vincule-o ao `<textarea>` com `id` e `for`.

2. **Estilo com CSS**:
   - Personalize o campo para combinar com o design do seu site.

   ```css
   textarea {
       border: 1px solid #ccc;
       padding: 10px;
       font-size: 16px;
   }
   ```

3. **Limites e Validações**:
   - Combine atributos como `maxlength` e `required` para controlar a entrada do usuário.

---

Com essas informações, você pode criar campos de texto multilinha interativos e funcionais em suas páginas HTML!
