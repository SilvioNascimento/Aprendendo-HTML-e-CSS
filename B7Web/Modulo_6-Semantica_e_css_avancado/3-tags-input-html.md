# Guia Completo das Tags `<input>` em HTML

## O que é a tag `<input>`?

A tag `<input>` é um dos elementos mais usados em formulários HTML. Ela permite a entrada de dados pelo usuário e possui vários tipos e propriedades que definem seu comportamento e aparência.

---

## Principais propriedades do `<input>`

- `type` — Define o tipo do campo de entrada (texto, senha, email, número, etc).
- `name` — Nome do campo, usado para identificar o dado enviado no formulário.
- `value` — Valor inicial do campo.
- `placeholder` — Texto exibido quando o campo está vazio, para orientar o usuário.
- `required` — Indica que o campo é obrigatório.
- `readonly` — Campo somente leitura, não pode ser editado.
- `disabled` — Campo desabilitado, não pode ser editado nem enviado.
- `maxlength` — Limita o número máximo de caracteres.
- `min` e `max` — Definem valores mínimos e máximos para inputs numéricos e de data.
- `step` — Define o intervalo entre valores válidos (ex: para números decimais).
- `pattern` — Expressão regular para validação do valor.
- `autocomplete` — Indica se o navegador deve sugerir preenchimento automático.
- `autofocus` — Define que o campo deve receber foco automático ao carregar a página.

---

## Principais tipos de `<input>` e exemplos

### 1. Texto (`type="text"`)

Campo de texto simples.

```html
<label for="nome">Nome:</label>
<input type="text" id="nome" name="nome" placeholder="Digite seu nome" required maxlength="50" />
```

### 2. Senha (`type="password"`)

Campo para senha, oculta os caracteres.

```html
<label for="senha">Senha:</label>
<input type="password" id="senha" name="senha" required />
```

### 3. Email (`type="email"`)

Campo para email, com validação básica de formato.

```html
<label for="email">Email:</label>
<input type="email" id="email" name="email" placeholder="exemplo@dominio.com" required />
```

### 4. Número (`type="number"`)

Campo para números, permite definir intervalo e passos.

```html
<label for="idade">Idade:</label>
<input type="number" id="idade" name="idade" min="1" max="120" step="1" required />
```

### 5. Data (`type="date"`)

Campo para seleção de data.

```html
<label for="nascimento">Data de nascimento:</label>
<input type="date" id="nascimento" name="nascimento" required />
```

### 6. Data e Hora Local (`type="datetime-local"`)

Campo para data e hora, sem fuso horário.

```html
<label for="evento">Data e hora do evento:</label>
<input type="datetime-local" id="evento" name="evento" required />
```

### 7. Hora (`type="time"`)

Campo para seleção de horário (hora e minutos).

```html
<label for="hora">Horário:</label>
<input type="time" id="hora" name="hora" required />
```

### 8. Checkbox (`type="checkbox"`)

Caixa de seleção.

```html
<label><input type="checkbox" name="termos" required /> Aceito os termos</label>
```

### 9. Radio (`type="radio"`)

Botões de opção (mutuamente exclusivos).

```html
<p>Gênero:</p>
<label><input type="radio" name="genero" value="masculino" required /> Masculino</label>
<label><input type="radio" name="genero" value="feminino" /> Feminino</label>
```

### 10. Botão (`type="button"`)

Botão genérico para ações via JavaScript.

```html
<input type="button" value="Clique aqui" onclick="alert('Botão clicado!')" />
```

### 11. Submit (`type="submit"`)

Botão para enviar formulário.

```html
<input type="submit" value="Enviar" />
```

### 12. Reset (`type="reset"`)

Botão para resetar o formulário.

```html
<input type="reset" value="Limpar" />
```

### 13. URL (`type="url"`)

Campo para endereço de site, valida formato.

```html
<label for="site">Website:</label>
<input type="url" id="site" name="site" placeholder="https://exemplo.com" />
```

### 14. Tel (`type="tel"`)

Campo para telefone.

```html
<label for="telefone">Telefone:</label>
<input type="tel" id="telefone" name="telefone" placeholder="(11) 99999-9999" />
```

### 15. Cor (`type="color"`)

Selecionador de cor.

```html
<label for="cor">Escolha uma cor:</label>
<input type="color" id="cor" name="cor" value="#ff0000" />
```

### 16. Arquivo (`type="file"`)

Para upload de arquivos.

```html
<label for="arquivo">Selecione um arquivo:</label>
<input type="file" id="arquivo" name="arquivo" />
```
