# 📝 Anotação sobre WebKit

WebKit não é um navegador, um framework ou uma linguagem de programação. **WebKit é um motor de renderização de navegadores** (em inglês, *browser engine*).

Pense nele como o "motor" de um carro: ele é o componente central que pega o código de um site (HTML, CSS, JavaScript) e o transforma na página visual e interativa que vemos na tela.

---

## 🤔 Um Pouco de História e Quem Usa o WebKit

A história do WebKit é crucial para entender a web de hoje.

1. **Origem:** O WebKit foi iniciado pela Apple em 2001 como uma "derivação" (fork) do motor KHTML, que pertencia ao projeto de código aberto KDE.
2. **A Era de Ouro:** Por muitos anos, o WebKit foi o motor mais dominante do mundo. Ele era usado por dois dos navegadores mais populares: o **Safari** (da Apple) e o **Google Chrome**. Isso significava que a grande maioria dos usuários da web acessava sites através do WebKit.
3. **A Grande Divisão (Fork):** Em 2013, o Google decidiu criar sua própria versão do WebKit, chamada **Blink**. Desde então, o Chrome e a maioria dos outros navegadores baseados em Chromium (como Microsoft Edge, Opera, Brave) usam o Blink, e não mais o WebKit.

### Quem Usa o WebKit Hoje (Maio de 2025)?

- **Apple Safari:** É o principal usuário. O Safari em macOS, iOS e iPadOS é movido pelo WebKit.
- **Todos os Navegadores no iOS e iPadOS:** A Apple exige que **todos** os navegadores na App Store (incluindo Chrome, Firefox, Edge, etc.) usem o motor WebKit em seus sistemas operacionais móveis. Portanto, o "Chrome no iPhone" na verdade usa o motor do Safari (WebKit), não o seu motor padrão (Blink).
- **Navegadores de Nicho:** Alguns navegadores para Linux e sistemas embarcados (como os de smart TVs e consoles de videogame) ainda utilizam o WebKit.

---

## 🚀 Por que o WebKit é Importante para Desenvolvedores?

Mesmo que muitos navegadores agora usem o Blink, o legado e a importância contínua do WebKit afetam diretamente o nosso trabalho.

### 1. O Legado do Prefixo `-webkit-`

Este é o ponto mais visível para os desenvolvedores. Como o WebKit era dominante, muitas novas funcionalidades do CSS foram implementadas primeiro nele de forma experimental, usando o prefixo `-webkit-`.

- **Exemplos Comuns:** `border-radius`, `box-shadow`, `transition`, `animation`, `linear-gradient`. Todas essas propriedades tiveram uma versão `-webkit-` antes de se tornarem um padrão oficial.
- **Herança do Blink:** Como o Blink é uma derivação do WebKit, ele herdou e continuou a dar suporte a muitos desses prefixos. É por isso que, até hoje, uma propriedade `-webkit-` muitas vezes funciona tanto no Safari quanto no Chrome/Edge.
- **Propriedades Não Padrão:** Existem também muitas propriedades úteis que são exclusivas do WebKit (e herdadas pelo Blink) e que não fazem parte do padrão CSS oficial, mas são amplamente utilizadas:
  - `-webkit-font-smoothing: antialiased;` (para suavizar fontes)
  - `-webkit-appearance: none;` (para remover estilos padrão de formulários)
  - `-webkit-tap-highlight-color: transparent;` (para remover o destaque ao tocar em links no mobile)
  - Estilização da barra de rolagem com `::-webkit-scrollbar`.

**Exemplo de código com prefixo:**

```css
.elemento-animado {
  /* Prefixo para garantir compatibilidade com navegadores antigos baseados em WebKit */
  -webkit-animation: minha-animacao 4s infinite;
  
  /* Sintaxe padrão, que deve vir por último */
  animation: minha-animacao 4s infinite;
}
```

**Prática Atual (2025):** Assim como nos degradês e animações, a necessidade de escrever esses prefixos manualmente diminuiu drasticamente. Ferramentas como **Autoprefixer** fazem esse trabalho automaticamente. O importante é saber por que eles existem.

### 2. Compatibilidade e Testes

A principal razão para um desenvolvedor se preocupar com o WebKit hoje é o **Safari**. Se um site funciona perfeitamente no Chrome/Edge (Blink) mas apresenta falhas visuais ou de comportamento no Safari (WebKit), a diferença entre os motores de renderização é quase sempre a causa.

**É essencial testar seus projetos no Safari** para garantir uma boa experiência para milhões de usuários de produtos Apple.

---

### **Tabela Comparativa Rápida: WebKit vs. Blink**

| **Característica** | **WebKit** | **Blink** |
|--------------------|------------|-----------|
| **Principal Navegador** | Safari | Google Chrome, Microsoft Edge, Opera |
| **Desenvolvido Por** | Principalmente pela Apple e comunidade de código aberto | Principalmente pelo Google e comunidade de código aberto |
| **Motor JavaScript** | JavaScriptCore | V8 |
| **Legado do Prefixo** | `-webkit-` (Origem) | `-webkit-` (Herdado e mantido) |
