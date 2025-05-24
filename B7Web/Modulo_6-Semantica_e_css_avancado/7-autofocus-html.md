# Guia sobre o atributo `autofocus` em HTML

## O que é o `autofocus`?

O atributo `autofocus` é um atributo booleano que pode ser adicionado a elementos de formulário, como `<input>`, `<textarea>`, `<select>`, entre outros.

Ele indica que o elemento deve receber automaticamente o foco assim que a página for carregada, facilitando a interação do usuário ao iniciar o preenchimento do formulário.

---

## Características do `autofocus`

- Só pode ser aplicado a um único elemento por página para evitar conflitos.
- O elemento que recebe o `autofocus` fica com o cursor ativo, pronto para digitação ou interação.
- Se houver vários elementos com `autofocus`, apenas o primeiro na ordem do documento terá efeito.
- Funciona na maioria dos navegadores modernos.

---

## Exemplos de uso

### Input com autofocus

```html
<label for="nome">Nome:</label>
<input type="text" id="nome" name="nome" autofocus />
```

### Textarea com autofocus

```html
<label for="mensagem">Mensagem:</label>
<textarea id="mensagem" name="mensagem" autofocus></textarea>
```

---

## Dicas para usar o `autofocus`

- Use com moderação, preferencialmente em formulários simples.
- Evite usar em múltiplos campos na mesma página.
- Pode ajudar na usabilidade, especialmente em formulários de login ou pesquisa.
- Em dispositivos móveis, o teclado pode abrir automaticamente ao focar o campo.
- Teste em diferentes navegadores para garantir compatibilidade.

---

## Complemento: Focar dinamicamente via JavaScript

Você também pode usar JavaScript para focar um elemento em qualquer momento:

```javascript
document.getElementById('nome').focus();
```
