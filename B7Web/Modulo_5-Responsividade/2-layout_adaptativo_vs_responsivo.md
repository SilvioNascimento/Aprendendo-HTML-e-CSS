
# Layout Adaptativo vs Layout Responsivo

## Definições

### Layout Adaptativo (Adaptive Design)

- Baseia-se em **pontos de interrupção fixos (breakpoints)** pré-definidos.
- Para cada breakpoint, o design adapta-se a um conjunto específico de larguras de tela.
- O layout é criado para **tamanhos de tela específicos**, podendo usar diferentes arquivos CSS.
- Muitas vezes usa **media queries** para carregar estilos diferentes em dispositivos específicos.

### Layout Responsivo (Responsive Design)

- Utiliza um **layout fluido e flexível** que se adapta a qualquer tamanho de tela.
- Baseado em **percentuais, unidades relativas** (como %, em, rem, vw, vh).
- Ajusta-se automaticamente a qualquer largura, sem a necessidade de pontos de interrupção fixos.
- Usa media queries para ajustes finos, mas o principal é o layout fluido.

---

## Características principais

| Característica          | Layout Adaptativo                      | Layout Responsivo                  |
|------------------------|--------------------------------------|----------------------------------|
| Flexibilidade          | Adaptado a telas específicas          | Adapta-se a qualquer tamanho     |
| Complexidade           | Mais complexo, vários layouts          | Mais simples e fluido             |
| Carga de recursos      | Pode carregar arquivos específicos por dispositivo | Carrega um único layout          |
| Tempo de desenvolvimento | Pode ser maior                      | Geralmente menor                  |
| Uso comum              | Projetos legados, apps móveis          | Sites modernos e aplicações web  |

---

## Vantagens e desvantagens

### Layout Adaptativo

- **Vantagens:**
  - Controle preciso do design para dispositivos populares.
  - Pode otimizar performance ao carregar menos recursos para dispositivos menores.

- **Desvantagens:**
  - Pode não funcionar bem em tamanhos intermediários ou incomuns.
  - Mais difícil de manter com muitos layouts.

### Layout Responsivo

- **Vantagens:**
  - Funciona para qualquer dispositivo e tamanho de tela.
  - Facilita manutenção e escalabilidade.
  - Melhor experiência do usuário geral.

- **Desvantagens:**
  - Pode ser menos otimizado para dispositivos muito específicos.
  - Requer atenção para performance em layouts muito complexos.

---

## Exemplos práticos

### Layout Adaptativo (CSS básico)

```css
/* Layout para telas pequenas */
.container {
  width: 320px;
}

/* Layout para tablets */
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}

/* Layout para desktops */
@media (min-width: 1024px) {
  .container {
    width: 1024px;
  }
}
```

### Layout Responsivo (CSS fluido)

```css
.container {
  width: 90%; /* ocupa 90% da largura da viewport */
  max-width: 1200px; /* limite máximo para telas grandes */
  margin: 0 auto;
}

@media (min-width: 768px) {
  .container {
    padding: 20px;
  }
}
```

---

## Quando usar cada um?

| Caso                                | Recomendações                   |
|------------------------------------|--------------------------------|
| Projeto com público-alvo muito específico e dispositivos limitados | Layout Adaptativo               |
| Projetos modernos, variados e escaláveis | Layout Responsivo              |
| Aplicações que precisam de máxima performance em dispositivos móveis | Layout Adaptativo (com cuidado)|
| Sites que precisam funcionar bem em qualquer tela e dispositivo | Layout Responsivo              |

---

## Recursos para estudo

- [Responsive Web Design Basics - Google Developers](https://developers.google.com/web/fundamentals/design-and-ux/responsive)
- [Adaptive Web Design by Aaron Gustafson](https://adaptivewebdesign.info/)
- [CSS-Tricks: Responsive vs Adaptive Design](https://css-tricks.com/responsive-vs-adaptive-design/)

---
