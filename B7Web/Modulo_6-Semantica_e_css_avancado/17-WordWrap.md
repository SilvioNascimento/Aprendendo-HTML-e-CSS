# 📝 Anotação CSS: Quebra de Linha com overflow-wrap (word-wrap)

Ao criar layouts, um problema comum é quando uma palavra muito longa ou uma string de caracteres sem espaços (como uma URL ou um token) "vaza" para fora de seu contêiner, quebrando o design. A propriedade `overflow-wrap` foi criada para resolver exatamente isso.

**Nota Importante:** A propriedade que muitos conhecem como `word-wrap` foi oficialmente renomeada para **`overflow-wrap`** nos padrões CSS. Embora `word-wrap` ainda funcione como um *alias* (apelido) para manter a compatibilidade com navegadores mais antigos, a boa prática hoje é usar `overflow-wrap` no seu código.

---

## O Problema: Quando o Texto "Vaza"

Imagine que você tem uma caixa com uma largura fixa, e um usuário insere um link muito longo em um comentário. O resultado pode ser este:

```html
<style>
  .caixa-problema {
    width: 250px;
    border: 2px solid #c92a2a;
    padding: 10px;
  }
</style>

<div class="caixa-problema">
  <p>Confira este link: https://www.exemplo.com/produtos/categoria/subcategoria/identificador-de-produto-extremamente-longo-e-sem-espacos</p>
</div>
```

O link, por ser uma "palavra" única e inquebrável, não respeita a largura da caixa e transborda, estragando o layout.

---

## A Solução: Usando overflow-wrap: `break-word`

A solução é aplicar `overflow-wrap` ao contêiner. O valor `break-word` instrui o navegador a, como último recurso, quebrar a palavra em qualquer ponto para evitar o transbordamento.

```html
<style>
  .caixa-solucao {
    width: 250px;
    border: 2px solid #12b886;
    padding: 10px;
    
    /* A SOLUÇÃO: */
    overflow-wrap: break-word;
  }
</style>

<div class="caixa-solucao">
  <p>Confira este link: https://www.exemplo.com/produtos/categoria/subcategoria/identificador-de-produto-extremamente-longo-e-sem-espacos</p>
</div>
```

Com essa única linha, o navegador irá quebrar o link longo, forçando-o a se ajustar dentro dos limites da caixa.

---

## Valores da Propriedade `overflow-wrap`

| **Valor** | **Descrição** |
|-----------|---------------|
| `normal` (Padrão) | Quebra linhas apenas em pontos de quebra permitidos (espaços, hífens, etc.). Palavras longas ainda podem transbordar. |
| `break-word` | Permite que palavras inquebráveis sejam quebradas em pontos arbitrários para evitar o transbordamento. Ele só faz isso se a palavra não couber em sua própria linha. |
| `anywhere` | Um valor mais recente e mais agressivo. Ele pode quebrar uma palavra em qualquer ponto se isso levar a uma melhor "aparência" do layout, mesmo que a palavra pudesse caber na próxima linha. É menos usado que `break-word`. |

---

## `overflow-wrap` vs. `word-break` (Uma Dúvida Comum)

É fácil confundir `overflow-wrap` com outra propriedade: `word-break`. Elas parecem fazer o mesmo, mas sua lógica é diferente.

* `overflow-wrap: break-word` (Plano B): Tenta primeiro quebrar o texto normalmente (usando espaços). Se uma palavra ainda for muito longa e estiver transbordando, **ela quebra apenas essa palavra.**
* `word-break: break-all` (Regra Agressiva): Não se importa com as regras normais de quebra. Ela quebra palavras em qualquer caractere para preencher o espaço, o que pode levar a quebras desnecessárias em textos normais.

### **Exemplo Comparativo:**

```html
<style>
  .caixa-exemplo { width: 150px; border: 1px solid #000; margin-bottom: 10px; padding: 5px; }
  .exemplo-overflow-wrap { overflow-wrap: break-word; }
  .exemplo-word-break { word-break: break-all; }
</style>

<p>Com <strong>overflow-wrap: break-word;</strong> (note como "Web" não quebra)</p>
<div class="caixa-exemplo exemplo-overflow-wrap">
  Aprenda Web com um supercalifragilisticexpialidocious.
</div>

<p>Com <strong>word-break: break-all;</strong> (note como "Web" quebra desnecessariamente)</p>
<div class="caixa-exemplo exemplo-word-break">
  Aprenda Web com um supercalifragilisticexpialidocious.
</div>
```

No primeiro exemplo, a palavra "Web" é movida inteira para a linha de baixo. No segundo, ela é quebrada ao meio (`W-eb`), pois `break-all` é mais agressivo.

---

## Conclusão e Recomendação

Para a maioria dos casos em que você precisa evitar que textos longos e sem espaços (como URLs ou tokens) quebrem seu layout, overflow-wrap: break-word; é a solução que você procura. É segura, previsível e age apenas quando estritamente necessário para prevenir o transbordamento.
