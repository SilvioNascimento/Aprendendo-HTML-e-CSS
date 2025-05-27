# 📝 Anotação CSS: Animações com @keyframes

Animações em CSS permitem criar sequências de movimento e transições de estilo em elementos HTML sem a necessidade de JavaScript. Elas oferecem um controle muito maior do que as `transitions`, permitindo múltiplos estágios, repetição e controle de direção.

O processo de criação de uma animação CSS consiste em duas partes principais:

1. **A regra `@keyframes`**: Onde você define os "quadros-chave" ou estágios da sua animação, especificando os estilos que o elemento deve ter em cada ponto da sequência.
2. **As propriedades `animation`**: Aplicadas ao elemento que você quer animar para controlar como a sequência de `@keyframes` deve ser executada (duração, repetição, velocidade, etc.).

---

## Passo a Passo: Criando uma Animação Simples

Vamos criar um efeito de "pulsação" em um elemento.

### Passo 1: Definir o "Roteiro" com `@keyframes`

Primeiro, criamos a regra `@keyframes` e damos um nome a ela, por exemplo, `pulsar`. Dentro dela, definimos os estilos para o início (`from` ou `0%`) e o fim (`to` ou `100%`) da animação.

```css
@keyframes pulsar {
  /* Estado inicial da animação */
  from {
    transform: scale(1.0); /* Tamanho normal */
    opacity: 1;
  }

  /* Estado final da animação */
  to {
    transform: scale(1.1); /* Aumenta o tamanho em 10% */
    opacity: 0.7;
  }
}
```

### Passo 2: Aplicar a Animação a um Elemento

Agora, selecionamos o elemento HTML e usamos as propriedades `animation` para "executar" o roteiro `pulsar` que criamos.

```css
<style>
  /* Define a animação (roteiro) */
  @keyframes pulsar {
    from { transform: scale(1.0); opacity: 1; }
    to { transform: scale(1.1); opacity: 0.7; }
  }

  .circulo-pulsante {
    width: 100px;
    height: 100px;
    background-color: #c92a2a;
    border-radius: 50%;

    /* Aplica a animação ao elemento */
    animation-name: pulsar;              /* Nome da animação criada com @keyframes */
    animation-duration: 1.5s;            /* Duração de um ciclo completo */
    animation-iteration-count: infinite; /* Repete a animação infinitamente */
    animation-direction: alternate;      /* Alterna a direção (ida e volta) */
    animation-timing-function: ease-in-out; /* Curva de velocidade suave */
  }
</style>

<div class="circulo-pulsante"></div>
```

**Resultado:** O círculo vermelho irá crescer e diminuir suavemente, de forma infinita, criando um efeito de pulsação.

---

## O Painel de Controle: Propriedades da Animação

Aqui estão as propriedades mais importantes para controlar suas animações:

|   **Propriedade** |   **Descrição**   |   **Exemplo de valor**    |
|-------------------|-------------------|-----------|
| `animation-name` | O nome da regra `@keyframes` que você quer usar. | `pulsar`, `deslizar` |
| `animation-duration` | Quanto tempo um ciclo da animação leva para ser concluído. | `2s`, `500ms` |
| `animation-timing-function` | A curva de velocidade da animação (aceleração). | `ease`, `linear`, `ease-in-out` |
| `animation-delay` | O tempo de espera antes de a animação começar. | `1s` (Espera 1 segundo) |
| `animation-iteration-count` | A direção em que a animação deve ser executada. | `normal`, `reverse`, `alternate` |
| `animation-fill-mode` | Define quais estilos são aplicados antes e depois da animação. | `forwards`, `backwards`, `both` |
| `animation-play-state` | Permite pausar (`paused`) ou executar (`running`) uma animação. | `paused` |

---

## **A Propriedade `animation` (Shorthand)**

Para economizar espaço, você pode combinar todas as propriedades acima em uma única declaração `animation`.

**Ordem:** `animation: [name] [duration] [timing-function] [delay] [iteration-count] [direction] [fill-mode];`

O exemplo do círculo pulsante poderia ser reescrito assim:

```css
.circulo-pulsante {
  /* ... outros estilos ... */
  animation: pulsar 1.5s ease-in-out infinite alternate;
}
```

---

## Animações vs. Transições (Transitions)

Embora parecidas, elas têm propósitos diferentes.

| **Característica** | **Transitions** | **Animations** |
|--------------------|-----------------|----------------|
| **Gatilho (Trigger)** | Requer uma mudança de estado (ex: `:hover`, clique via JS, mudança de classe). | Pode começar automaticamente assim que a página carrega, sem necessidade de gatilho. |
| **Complexidade** | Simples. Transição de um estado A para um estado B. | Complexa. Permite múltiplos estágios (`0%`, `50%`, `100%`) definidos em `@keyframes`. |
| **Repetição** | Não repete automaticamente. | Pode repetir um número definido de vezes ou infinitamente (`infinite`). |
| **Uso Ideal** | Para feedback de interações do usuário, como botões, links e menus. | Para sequências de movimento contínuas, loaders, banners e efeitos visuais complexos. |

### Dica de Performance

Para animações mais suaves e performáticas, dê preferência a animar as propriedades `transform` (como `translate`, `scale`, `rotate`) e `opacity`. Animar propriedades que afetam o layout (como `width`, `height`, `margin`, `top`, `left`) pode ser mais custoso para o navegador e causar "engasgos".

---

## Exemplo Prático Avançado: Animação de Texto "Carregando..."

Agora que entendemos os conceitos, vamos aplicá-los em um exemplo mais elaborado, como o efeito de "onda" em um texto de carregamento.

### **Estratégia**

1. **Isolar cada caractere:** Para animar cada letra individualmente, vamos envolvê-la em uma tag `<span>`.
2. **Criar a animação:** Faremos uma regra `@keyframes` que levanta a letra (`transform: translateY()`) e muda sua `color` no meio do ciclo.
3. **Criar o efeito de onda:** O segredo é aplicar um `animation-delay` (atraso) diferente para cada letra, fazendo com que uma comece a se mover um pouco depois da anterior.

#### **Passo 1: O HTML**

Estruturamos o texto com cada caractere dentro de um `<span>`.

```html
<div class="loading-text">
  <span>C</span><span>a</span><span>r</span><span>r</span><span>e</span><span>g</span><span>a</span><span>n</span><span>d</span><span>o</span><span>.</span><span>.</span><span>.</span>
</div>
```

#### **Passo 2: O CSS**

Agora, criamos a animação e aplicamos os atrasos progressivos.

```html
<style>
  .loading-text {
    font-size: 2rem; /* Tamanho da fonte */
    font-family: sans-serif;
    font-weight: bold;
    text-align: center;
  }

  /* Define a animação que será usada por cada letra */
  @keyframes onda-de-texto {
    0% {
      transform: translateY(0);
      color: #000000; /* Cor preta inicial */
    }
    50% {
      /* Ponto alto da animação: letra se levanta e muda de cor */
      transform: translateY(-15px); /* Sobe 15 pixels */
      color: #c92a2a; /* Cor vermelha para destaque */
    }
    100% {
      /* Volta ao estado inicial */
      transform: translateY(0);
      color: #000000;
    }
  }

  /* Estilos base para cada letra (<span>) */
  .loading-text span {
    display: inline-block; /* Permite o uso de transform */
    animation-name: onda-de-texto;
    animation-duration: 1.8s; /* Duração de um ciclo completo */
    animation-iteration-count: infinite; /* Repete para sempre */
    animation-timing-function: ease-in-out; /* Curva de velocidade suave */
  }

  /* O TRUQUE: Atraso progressivo para cada letra criar o efeito de onda */
  .loading-text span:nth-child(1) { animation-delay: 0.1s; }
  .loading-text span:nth-child(2) { animation-delay: 0.2s; }
  .loading-text span:nth-child(3) { animation-delay: 0.3s; }
  .loading-text span:nth-child(4) { animation-delay: 0.4s; }
  .loading-text span:nth-child(5) { animation-delay: 0.5s; }
  .loading-text span:nth-child(6) { animation-delay: 0.6s; }
  .loading-text span:nth-child(7) { animation-delay: 0.7s; }
  .loading-text span:nth-child(8) { animation-delay: 0.8s; }
  .loading-text span:nth-child(9) { animation-delay: 0.9s; }
  .loading-text span:nth-child(10) { animation-delay: 1.0s; }
  .loading-text span:nth-child(11) { animation-delay: 1.1s; }
  .loading-text span:nth-child(12) { animation-delay: 1.2s; }
  .loading-text span:nth-child(13) { animation-delay: 1.3s; }

</style>
```
