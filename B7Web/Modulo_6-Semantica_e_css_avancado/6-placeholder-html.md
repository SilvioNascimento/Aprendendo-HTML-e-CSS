# Guia sobre o atributo `placeholder` em HTML

## O que é o `placeholder`?

O atributo `placeholder` é usado em elementos de formulário, principalmente `<input>` e `<textarea>`, para exibir um texto de exemplo dentro do campo quando ele está vazio.

Esse texto serve como uma dica ou orientação para o usuário sobre o que deve ser preenchido naquele campo.

---

## Características do `placeholder`

- Aparece somente quando o campo está vazio e não focado.
- Desaparece assim que o usuário começa a digitar.
- Não é um valor do campo — não é enviado no formulário se o usuário não digitar nada.
- Deve ser claro e curto para ser efetivo como dica.

---

## Exemplos de uso

### Input de texto com placeholder

```html
<label for="nome">Nome:</label>
<input type="text" id="nome" name="nome" placeholder="Digite seu nome completo" />
```

### Textarea com placeholder

```html
<label for="mensagem">Mensagem:</label>
<textarea id="mensagem" name="mensagem" placeholder="Escreva sua mensagem aqui..."></textarea>
```

### Input de email com placeholder

```html
<input type="email" name="email" placeholder="exemplo@dominio.com" />
```

---

## Dicas para usar placeholder

- Use para orientar o preenchimento, mas nunca substitua um rótulo (`label`).
- Evite usar placeholders como única forma de identificação do campo, pois prejudica a acessibilidade.
- Mantenha o texto do placeholder curto e direto.
- Para melhorar a experiência em acessibilidade, combine `label` com `placeholder`.
- Em alguns navegadores e dispositivos, o placeholder pode ter estilo diferenciado (cor cinza clara, por exemplo).

---

## Customizando o estilo do placeholder com CSS

Você pode alterar a aparência do placeholder usando pseudo-classes:

```css
input::placeholder,
textarea::placeholder {
  color: #888888;
  font-style: italic;
}
```
