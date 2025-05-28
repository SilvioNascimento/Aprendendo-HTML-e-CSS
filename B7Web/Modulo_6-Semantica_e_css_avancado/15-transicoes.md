# 📝 Anotação CSS: Transições (Transitions)

As transições em CSS (`transitions`) são uma maneira de animar suavemente a mudança de uma propriedade CSS de um valor para outro ao longo de um período de tempo. Em vez de uma alteração instantânea e "dura", a transição cria um efeito gradual e agradável.

Diferente das `animations`, as transições precisam de um **gatilho (trigger)** para serem iniciadas. O gatilho mais comum é uma mudança de estado, como quando o usuário passa o mouse sobre um elemento (`:hover`) ou quando uma classe é adicionada via JavaScript.

---

## Como Funcionam as Transições? (O Básico)

O processo envolve dois estados:

1. **O Estado Inicial:** É o estado padrão do elemento. É aqui que você define a propriedade `transition`, especificando *qual* propriedade CSS deve ser animada e *por quanto tempo*.
2. **O Estado Final:** É o estado ativado pelo gatilho (ex: `:hover`). Aqui, você apenas define o novo valor para a propriedade que deseja alterar. O navegador cuidará da animação suave entre os dois estados.

### Exemplo Prático: Um Botão Interativo

Vamos criar um botão que muda de cor e de tamanho suavemente ao passar o mouse sobre ele.

```html
<style>
  .botao-transicao {
    background-color: #4c6ef5;
    color: white;
    padding: 15px 30px;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    cursor: pointer;

    /* PASSO 1: Definimos a transição no estado inicial.
      - Quais propriedades? 'background-color', 'transform'.
      - Qual a duração? 0.4 segundos.
      - Qual a curva de velocidade? 'ease'.
    */
    transition: background-color 0.4s ease, transform 0.4s ease;
  }

  /*
    PASSO 2: Definimos o estado final, que será o gatilho.
    Nós apenas mudamos os valores finais das propriedades.
    O navegador usará as regras de 'transition' acima para animar a mudança.
  */
  .botao-transicao:hover {
    background-color: #364fc7;
    transform: scale(1.1); /* Aumenta o tamanho do botão em 10% */
  }
</style>

<button class="botao-transicao">Passe o mouse aqui!</button>
```

**Resultado:** Ao passar o mouse, o botão não mudará de cor e tamanho instantaneamente. Ele fará uma transição suave de 0.4 segundos para o novo estado. Ao retirar o mouse, ele retornará suavemente ao estado original.

---

## O Painel de Controle: As Propriedades da Transição

Existem quatro propriedades principais que controlam uma transição.

| **Propriedade** | **Descrição** | **Exemplo de Valor** |
|-----------------|---------------|----------------------|
| `transition-property` | Especifica **qual** propriedade CSS será transicionada. | `width`, `background-color`, `transform`, `all` |
| `transition-duration` | **Obrigatória**. Define **quanto tempo** a transição levará. | `0.5s`, `300ms` |
| `transition-timing-function` | A curva de velocidade (aceleração) da transição. | `ease`, `linear`, `ease-in`, `ease-out`, `ease-in-out` |
| `transition-delay` | Um tempo de espera **antes** que a transição comece. | `1s` (espera 1 segundo para iniciar) |

---

## A Propriedade `transition` (Shorthand)

É muito mais comum usar a propriedade `transition` para combinar tudo em uma única linha.

**Ordem:** `transition: [property] [duration] [timing-function] [delay];`

O exemplo do botão poderia ser simplificado assim:

```css
.botao-transicao {
  /* ... outros estilos ... */
  transition: all 0.4s ease-in-out;
}

.botao-transicao:hover {
  background-color: #364fc7;
  transform: scale(1.1);
}
```

Aqui, usamos `all` para indicar que queremos transicionar todas as propriedades que mudarem no estado `:hover`.

---

## Transicionando Múltiplas Propriedades com Configurações Diferentes

Você pode definir durações e curvas de velocidade diferentes para cada propriedade, separando-as por vírgula.

```css
.caixa-multipla {
  width: 100px;
  height: 100px;
  background-color: #12b886;
  opacity: 0.5;

  /* A cor de fundo mudará rápido, mas a opacidade mudará lentamente */
  transition: background-color 0.2s linear, opacity 1s ease-out;
}

.caixa-multipla:hover {
  background-color: #c92a2a;
  opacity: 1;
}
```

## O que pode (e não pode) ser Transicionado?

Nem toda propriedade CSS pode ser animada. Apenas propriedades que têm um valor intermediário podem ser transicionadas.

* ✅ **Pode Transicionar:** `width`, `height`, `color`, `background-color`, `opacity`, `font-size`, `border-radius`, `transform`, etc.
* ❌ **Não Pode Transicionar:** `display` (não há um meio-termo entre `none` e `block`), `font-family`, `position` (na maioria dos casos), etc. A mudança para essas propriedades será sempre instantânea.

## Dica de Performance

Assim como nas `animations`, para transições extremamente suaves, especialmente em dispositivos móveis, dê preferência a transicionar as propriedades `transform` e `opacity`. Elas são otimizadas pelos navegadores e não forçam o recálculo do layout da página, resultando em uma animação mais fluida.
