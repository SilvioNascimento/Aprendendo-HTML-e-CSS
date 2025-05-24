# Guia dos Atributos `size` e `maxlength` em HTML

Ao trabalhar com formulários em HTML, especialmente com a tag `<input>`, dois atributos que frequentemente causam confusão são `size` e `maxlength`. Embora ambos usem um valor numérico, suas funções são completamente diferentes.

Este guia irá detalhar cada um deles, mostrar as diferenças cruciais e explicar quando usar cada um.

---

## Atributo `size`

O atributo `size` controla a __largura visual__ de um campo de input, medida em número de caracteres. É um atributo puramente de apresentação.

### Propósito e Características de `size`

- __Controle Visual:__ Define o quão largo o campo de input aparecerá na tela. Por exemplo, `size="20"` cria um campo com a largura aproximada de 20 caracteres.
- __Não Limita a Entrada:__ O usuário pode digitar quantos caracteres quiser, independentemente do valor de `size`. Se o texto for maior que a largura do campo, o texto irá rolar horizontalmente dentro dele.
- __Valor Numérico:__ O valor deve ser um número inteiro positivo.

### Sintaxe de `size`

```html
<input type="text" size="valor_numerico">
```

#### Exemplo prático de `size`

Imagine que você quer um campo para nome e outro para sobrenome, mas quer que o campo de nome seja visualmente maior.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <title>Exemplo de Size</title>
    <style>
        body { font-family: sans-serif; }
        label { display: block; margin: 10px 0 5px 0; }
    </style>
</head>
<body>
    <h2>Formulário de Cadastro</h2>

    <label for="nome">Nome:</label>
    <input type="text" id="nome" name="nome" size="30">

    <label for="sobrenome">Sobrenome:</label>
    <input type="text" id="sobrenome" name="sobrenome" size="15">
</body>
</html>
```

__Resultado:__ O campo "Nome" será visivelmente mais largo que o campo "Sobrenome", mas em ambos você poderá digitar um texto de qualquer comprimento.

---

## Atributo `maxlength`

O atributo `maxlength` define o __número máximo de caracteres__ que o navegador permitirá que o usuário digite dentro do campo. É um atributo de validação e restrição de dados.

### Propósito e Características da `maxlength`

- __Validação de Dados:__ É usado para garantir que os dados inseridos não excedam um limite específico.
- __Limite Rígido:__ O navegador impede fisicamente que o usuário digite mais caracteres do que o valor definido no `maxlength`. Não é necessário JavaScript para essa validação básica.
- __Feedback Imediato:__ O usuário percebe o limite na hora, pois simplesmente não consegue mais digitar.

### Sintaxe da `maxlength`

```html
<input type="text" maxlength="valor_numerico">
```

#### Exemplo Prático de `maxlength`

Um caso de uso perfeito é para campos com formato fixo, como CEP (no Brasil, 8 dígitos) ou a sigla de um estado (UF, 2 dígitos).

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <title>Exemplo de MaxLength</title>
    <style>
        body { font-family: sans-serif; }
        label { display: block; margin: 10px 0 5px 0; }
    </style>
</head>
<body>
    <h2>Endereço</h2>

    <label for="cep">CEP (apenas números):</label>
    <input type="text" id="cep" name="cep" maxlength="8">

    <label for="uf">Estado (UF):</label>
    <input type="text" id="uf" name="uf" maxlength="2">
</body>
</html>
```

__Resultado:__ No campo "CEP", a digitação irá parar no 8º caractere. No campo "Estado (UF)", a digitação irá parar no 2º caractere.

---

## A Diferença Crucial: `size` vs. `maxlength`

A melhor forma de entender é vê-los juntos. Pense no `size` como o __tamanho da janela__ e no `maxlength` como o __limite de pessoas__ que podem entrar na sala. A janela pode ser pequena, mas muitas pessoas podem entrar e ficar na sala.

### Exemplo Combinado

Vamos criar um campo para um comentário que é visualmente pequeno (`size="20"`) mas permite até 140 caracteres (`maxlength="140"`).

```html
<label for="comentario">Deixe seu comentário (máx 140 caracteres):</label>
<input type="text" id="comentario" name="comentario" size="20" maxlength="140">
```

Neste caso:

1. O campo aparecerá na tela com a largura de apenas 20 caracteres.
2. O usuário poderá digitar até 140 caracteres.
3. A partir do 21º caractere, o texto começará a rolar para a esquerda dentro do campo.

### Tabela comparativa

| __Característica__ | __`size`__ | __`maxlength`__ |
|--------------------|------------|-----------------|
| __Função principal__ | Apresentação Visual | Validação de Dados |
| __O que faz?__ | Define a largura visível do campo. | Define o número máximo de caracteres. |
| __Tipo de Controle__ | Controle de layout (CSS faz isso melhor). | Restrição de entrada de dados do usuário. |
| __Comportamento__ | O texto rola se for maior que o `size`. | Impede a digitação além do limite. |

## A quais tipos de input se aplicam?

Ambos os atributos `size` e `maxlength` se aplicam aos seguintes tipos de `<input>`:

- `text`;
- `search`;
- `url`;
- `tel`;
- `email`;
- `password`;

## Conclusão

- Use `size` quando quiser sugerir uma largura visual para um campo, mas lembre-se que o CSS (`width`) é geralmente a ferramenta mais poderosa e flexível para isso.
- Use `maxlength` sempre que precisar impor um limite rígido no comprimento dos dados para garantir a integridade da informação, como em códigos postais, siglas, números de documento, etc.
