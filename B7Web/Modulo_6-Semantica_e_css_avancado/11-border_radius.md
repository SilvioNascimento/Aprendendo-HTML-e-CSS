# 📝 Anotação CSS: Bordas Arredondadas com `border-radius`

Uma das propriedades mais fundamentais e utilizadas no design web moderno é a `border-radius`. Ela permite suavizar os cantos de qualquer elemento que tenha uma borda, criando desde sutis arredondamentos até formas completamente circulares.

---

## Sintaxe Básica (Um valor para todos os cantos)

A forma mais comum de usar `border-radius` é aplicando um único valor, que será usado para arredondar os quatro cantos do elemento de maneira uniforme.

- **Propriedade:** `border-radius`
- **Valores:** Unidades como `px`, `em`, `rem`, `%`.

**Exemplo:**

```html
<style>
  .caixa-arredondada {
    border: 2px solid #0056b3;
    padding: 20px;
    width: 200px;
    height: 100px;
    /* Aplica um raio de 15 pixels para todos os quatro cantos */
    border-radius: 15px;
  }
</style>

<div class="caixa-arredondada">
  Este elemento tem cantos suavemente arredondados.
</div>
```

---

## Controlando Cada Canto Individualmente

A propriedade `border-radius` é uma "shorthand" (atalho) e pode aceitar de um a quatro valores para controlar cada canto de forma independente, seguindo a ordem do relógio (horário).

- **Ordem:** Canto Superior Esquerdo → Canto Superior Direito → Canto Inferior Direito → Canto Inferior Esquerdo.

| Valores Fornecidos | Resultado                                                                 |
| ------------------ | ------------------------------------------------------------------------- |
| **1 valor:** | `border-radius: 10px;` (Todos os cantos com 10px)                         |
| **2 valores:** | `border-radius: 10px 30px;` (Superior esquerdo/Inferior direito com 10px, Superior direito/Inferior esquerdo com 30px) |
| **3 valores:** | `border-radius: 10px 30px 50px;` (Superior esquerdo 10px, Superior direito/Inferior esquerdo 30px, Inferior direito 50px) |
| **4 valores:** | `border-radius: 10px 30px 50px 5px;` (Cada canto com seu valor, em ordem horária) |

**Exemplo com 4 valores:**

```css
.caixa-maluca {
  /* 10px sup-esq, 30px sup-dir, 50px inf-dir, 5px inf-esq */
  border-radius: 10px 30px 50px 5px;
  border: 2px solid #c92a2a;
  padding: 20px;
  text-align: center;
}
```

---

## Propriedades Específicas (Long-hand)

Se preferir, ou se precisar de mais clareza no seu código, você pode definir o raio de cada canto com sua própria propriedade:

- `border-top-left-radius`
- `border-top-right-radius`
- `border-bottom-right-radius`
- `border-bottom-left-radius`

**Exemplo:**

```css
.aba-de-navegacao {
  background-color: #f1f3f5;
  border: 1px solid #dee2e6;
  /* Arredonda apenas os cantos superiores para criar um efeito de aba */
  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
}
```

---

## Formas Criativas e Casos de Uso

A `border-radius` vai muito além de simples caixas.

### **Criando um Círculo**

Para criar um círculo perfeito, use um elemento quadrado (`width` e `height` iguais) e defina o `border-radius` como `50%`.

```css
.circulo {
  width: 150px;
  height: 150px;
  background-color: #4c6ef5;
  /* O valor 50% garante um círculo perfeito */
  border-radius: 50%;
}
```

### **Criando um "Pill Shape" (Formato de Pílula)**

Ideal para botões. Use um valor de `border-radius` bem alto. Um truque comum é usar um valor grande como `9999px` para garantir que as extremidades sejam sempre perfeitamente redondas, independentemente da largura do elemento.

```css
.botao-pilula {
  display: inline-block;
  padding: 12px 24px;
  background-color: #12b886;
  color: white;
  text-decoration: none;
  font-weight: bold;
  border-radius: 9999px;
}
```

### **Dica Avançada: Raios Elípticos**

Você pode criar cantos elípticos (ovais) fornecendo dois valores por canto, separados por uma barra `/`. O primeiro valor é o raio horizontal e o segundo é o raio vertical.

```css
.forma-organica {
  /* Sintaxe: [raios horizontais] / [raios verticais] */
  border-radius: 40% 60% 70% 30% / 50% 70% 30% 50%;
  width: 200px;
  height: 200px;
  background: linear-gradient(45deg, #fd7e14, #f76707);
}
```

Este recurso permite a criação de formas muito mais complexas e orgânicas diretamente com CSS.
