# 📝 Anotação HTML: Citações com `<blockquote>`, `<q>` e `<cite>`

Para marcar citações em HTML, não basta apenas usar aspas ou colocar o texto em itálico. Existem tags específicas que dão significado semântico ao conteúdo, informando ao navegador e a tecnologias assistivas que aquele trecho é uma citação.

As três principais tags relacionadas a citações são `<blockquote>`, `<q>` e `<cite>`.

---

## 1. Citações em Bloco: `<blockquote>`

Use a tag `<blockquote>` para citações longas ou que representam um bloco de conteúdo independente. Ela é ideal para destacar um parágrafo inteiro ou múltiplos parágrafos que foram retirados de outra fonte.

- **Nível:** Bloco (Block-level). Ela ocupa sua própria "linha" e cria um novo bloco de formatação.
- **Aparência Padrão:** Os navegadores geralmente renderizam o `<blockquote>` com um recuo (margem) nas laterais para destacá-lo visualmente do texto ao redor.
- **Atributo `cite`:** Você pode (e deve) usar o atributo `cite` para fornecer a URL da fonte da citação. Este link não é visível para o usuário, mas é útil para SEO e acessibilidade.

### Exemplo de Uso

```html
<p>Recentemente, li uma passagem sobre a importância da curiosidade que me marcou profundamente:</p>

<blockquote cite="https://www.exemplo.com/fonte-do-artigo">
  <p>A curiosidade tem sua própria razão de existir. Uma pessoa não pode deixar de se maravilhar ao contemplar os mistérios da eternidade, da vida, da estrutura maravilhosa da realidade.</p>
  <p>Nunca perca uma santa curiosidade.</p>
</blockquote>

<footer>
  <p>— Albert Einstein em uma conversa com William Miller, publicada na revista <cite>LIFE</cite>.</p>
</footer>
```

#### **Análise do Exemplo:**

- O `<blockquote>` agrupa a citação longa como um bloco separado.
O atributo cite aponta para a fonte online.
- A tag `<footer>` é usada aqui para fornecer informações de atribuição sobre a citação. É uma prática comum e semanticamente correta.
- A tag `<cite>` é usada corretamente para citar o título da obra (a revista LIFE), e não o autor. Veremos mais sobre isso abaixo.

---

## 2. Citações em Linha: `<q>`

Use a tag `<q>` para citações curtas que fazem parte de um parágrafo ou de uma frase.

- **Nível:** Linha (Inline). Ela é inserida no meio de um fluxo de texto.
- **Aparência Padrão:** A grande vantagem da tag `<q>` é que **o navegador adiciona as aspas automaticamente**. Isso é semanticamente correto e evita problemas com diferentes idiomas, que podem usar aspas diferentes (ex: “ ” vs. « »).
- **Atributo cite:** Assim como `<blockquote>`, também pode ter um atributo cite com a URL da fonte.

### Exemplo de uso

```html
<p>Como o famoso ditado nos lembra, <q>a imaginação é mais importante que o conhecimento</q>. Essa ideia nos incentiva a nunca parar de sonhar e criar.</p>
```

**Resultado:** O navegador irá renderizar: Como o famoso ditado nos lembra, "a imaginação é mais importante que o conhecimento". Essa ideia nos incentiva a nunca parar de sonhar e criar.

---

## 3. Citando a Fonte: `<cite>` (E o Erro Comum)

Esta é a tag que mais causa confusão.

A tag `<cite>` **NÃO** deve ser usada para o nome da pessoa que disse a frase. Ela serve, especificamente, para citar o **título de uma obra criativa**.

**Use o `<cite>` para:**

- Títulos de livros (ex: `<cite>O Guia do Mochileiro das Galáxias</cite>`)
- Títulos de filmes (ex: `<cite>Interestelar</cite>`)
- Nomes de músicas ou álbuns
- Nomes de peças de teatro, poemas, pinturas, etc.
- Nomes de programas de TV ou artigos de jornais.

**Aparência Padrão:** O conteúdo da tag `<cite>` é geralmente renderizado em itálico.

### **Como Fazer Certo (e Errado)**

- ❌ **JEITO ERRADO:** `<p>Como disse <cite>Santos Dumont</cite>, ...</p>`

- ✅ **JEITO CERTO:** `<p>Como disse Santos Dumont, ...</p>` (O nome de uma pessoa não precisa de uma tag semântica especial nesse contexto).

- ✅ **USO CORRETO DA TAG `<cite>`:** `<p>O meu filme favorito sobre o espaço é <cite>2001: Uma Odisseia no Espaço</cite>.</p>`

---

## **Tabela Resumo Rápida**

| **Tag** | **Uso Semântico** | **Aparência Padrão** |
|---------|-------------------|----------------------|
| `<blockquote>` | Para uma citação longa, que forma seu próprio bloco de texto. | Recuado (com margens). |
| `<q>` | Para uma citação curta, que está dentro de uma frase. | Adiciona aspas automaticamente. |
| `<cite>` | Para o **título de uma obra criativa** (livro, filme, etc.). | Texto em itálico. |

## Conclusão

Usar as tags de citação corretamente enriquece o significado do seu documento. `<blockquote>` para blocos, `<q>` para trechos em linha e `<cite>` estritamente para títulos de obras. Essa prática melhora a acessibilidade, a clareza do código e a forma como os motores de busca interpretam seu conteúdo.
