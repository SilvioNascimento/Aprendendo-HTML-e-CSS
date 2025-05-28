# 📝 Anotação CSS: Sombras com box-shadow e text-shadow

Em CSS, podemos aplicar efeitos de sombra a dois tipos de elementos: aos "objetos" ou "caixas" (como `div`, `button`, `img`) e diretamente aos caracteres de um texto. Para isso, usamos duas propriedades distintas, mas com uma sintaxe parecida: `box-shadow` e `text-shadow`.

---

## 1. Sombra de Caixas (`box-shadow`)

A propriedade `box-shadow` adiciona uma ou mais sombras à caixa de um elemento. É extremamente versátil para criar desde sutis elevações até efeitos de iluminação complexos.

### Sintaxe Detalhada

A sintaxe básica é a seguinte:
`box-shadow: [offset-x] [offset-y] [blur-radius] [spread-radius] [color] [inset];`

- `offset-x`: Deslocamento horizontal. Um valor positivo move a sombra para a direita; um negativo, para a esquerda.
- `offset-y`: Deslocamento vertical. Um valor positivo move a sombra para baixo; um negativo, para cima.
- `blur-radius` (opcional): O raio de desfoque. Quanto maior o valor, mais borrada e suave a sombra se torna. O valor `0` cria uma sombra nítida.
- `spread-radius` (opcional): O raio de expansão. Um valor positivo aumenta o tamanho da sombra; um negativo, a diminui.
- `color` (opcional): A cor da sombra. É uma boa prática sempre definir uma cor. Usar cores semitransparentes (ex: `rgba(0, 0, 0, 0.2)`) cria efeitos mais realistas.
- `inset` (opcional): Palavra-chave que, se presente, transforma a sombra externa (drop-shadow) em uma sombra interna, criando um efeito de "profundidade" ou "entalhe".

### Exemplo Básico

```html
<style>
  .cartao {
    width: 250px;
    padding: 20px;
    background-color: white;
    border-radius: 8px;
    /* offset-x | offset-y | blur | spread | color */
    box-shadow: 5px 10px 15px 0px rgba(0, 0, 0, 0.15);
  }
</style>

<div class="cartao">Este é um cartão com uma sombra suave.</div>
```

### A Sombra Interna (`inset`)

O `inset` é perfeito para simular painéis pressionados ou campos de formulário.

```css
.painel-pressionado {
  padding: 20px;
  background-color: #e9ecef;
  border-radius: 8px;
  /* A palavra-chave "inset" muda tudo */
  box-shadow: inset 3px 3px 7px rgba(0, 0, 0, 0.2);
}
```

### Múltiplas Sombras

Você pode criar efeitos de profundidade muito mais realistas empilhando várias sombras, separadas por vírgula. A primeira sombra da lista fica na camada de cima.

```css
.botao-realista {
  /* ... outros estilos de botão ... */
  /* Sombra 1: mais escura e próxima | Sombra 2: mais clara e distante */
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1),
              0 1px 3px rgba(0, 0, 0, 0.08);
}
```

---

## 2. Sombra de Textos (`text-shadow`)

A propriedade `text-shadow` funciona de forma parecida, mas aplica a sombra diretamente aos caracteres do texto, e não à caixa do elemento.

### Sintaxe Detalhada

A sintaxe é mais simples, pois não há `spread` nem `inset`:

`text-shadow: [offset-x] [offset-y] [blur-radius] [color];`

- `offset-x`: Deslocamento horizontal.
- `offset-y`: Deslocamento vertical.
- `blur-radius` (opcional): O raio de desfoque.
- `color` (opcional): A cor da sombra.

### Exemplo Básico

```css
.titulo-destacado {
  font-size: 3rem;
  font-weight: bold;
  /* offset-x | offset-y | blur | color */
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
}
```

### Efeitos Criativos com `text-shadow`

#### **Efeito de Contorno (Outline)**

Empilhando múltiplas sombras nítidas (sem blur) em várias direções, você pode criar um contorno.

```css
.texto-contornado {
  color: white;
  text-shadow:
   -1px -1px 0 #000, /* Cima-Esquerda */
    1px -1px 0 #000, /* Cima-Direita */
   -1px  1px 0 #000, /* Baixo-Esquerda */
    1px  1px 0 #000; /* Baixo-Direita */
}
```

#### **Efeito de Brilho (Glow / Neon)**

Usando um raio de desfoque (`blur-radius`) sem deslocamento (`offset`), você cria um efeito de brilho.

```css
.texto-neon {
  color: #fff;
  background-color: #181818; /* Fundo escuro para contraste */
  text-shadow: 0 0 10px #fff,
               0 0 20px #fff,
               0 0 30px #e60073,
               0 0 40px #e60073;
}
```

---

### Tabela Comparativa Rápida

| **Característica** | `box-shadow` | `text-shadow` |
|--------------------|--------------|---------------|
| **Aplica-se a** | À "caixa" do elemento HTML. | Aos caracteres do texto.|
| **Sintaxe Básica** | `offset-x` `offset-y` `blur` `spread` `color` | `offset-x` `offset-y` `blur` `color` |
| **Possui `spread`?** | Sim | Não |
| **Possui `inset`?** | Sim | Não |

### Dica de Performance

Sombras, especialmente `box-shadow` com grandes raios de desfoque e expansão, podem ser custosas para o navegador renderizar. Em elementos que são animados, use-as com moderação para garantir uma experiência fluida para o usuário.
