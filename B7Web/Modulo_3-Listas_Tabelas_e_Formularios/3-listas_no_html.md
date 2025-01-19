
# Trabalhando com Listas no HTML

O HTML oferece suporte a diferentes tipos de listas para organizar e exibir informações. As listas podem ser **desordenadas**, **ordenadas**, ou até mesmo **listas aninhadas** (listas dentro de listas).

---

## **1. Lista Desordenada**

As listas desordenadas (`<ul>`) exibem itens sem uma ordem específica. Cada item é representado pela tag `<li>`.

### **Exemplo Básico**
```html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```

### **Personalizando o Estilo da Lista: `list-style-type`**

A propriedade `list-style-type` em CSS permite alterar o marcador (bullet) usado nas listas desordenadas.

| **Valor**       | **Descrição**                          |
|------------------|----------------------------------------|
| `disc`          | Padrão, exibe marcadores preenchidos.  |
| `circle`        | Exibe marcadores circulares vazados.   |
| `square`        | Exibe marcadores quadrados.            |
| `none`          | Remove os marcadores da lista.         |

#### **Exemplo de Uso**
```html
<ul style="list-style-type: circle;">
    <li>Item com marcador circular</li>
    <li>Outro item com marcador circular</li>
</ul>
```

---

## **2. Lista Ordenada**

As listas ordenadas (`<ol>`) exibem itens em uma sequência específica, com números ou outros tipos de marcadores.

### **Exemplo Básico**
```html
<ol>
    <li>Primeiro item</li>
    <li>Segundo item</li>
    <li>Terceiro item</li>
</ol>
```

### **Personalizando o Estilo da Lista Ordenada**

1. **Atributo `type`**: Define o tipo de marcador usado.
   | **Valor** | **Descrição**                      |
   |-----------|------------------------------------|
   | `1`       | Números (padrão).                 |
   | `A`       | Letras maiúsculas (A, B, C...).   |
   | `a`       | Letras minúsculas (a, b, c...).   |
   | `I`       | Numerais romanos maiúsculos.      |
   | `i`       | Numerais romanos minúsculos.      |

2. **Atributo `start`**: Define o número inicial da contagem.

#### **Exemplo de Uso**
```html
<ol type="A" start="3">
    <li>Terceira letra</li>
    <li>Quarta letra</li>
    <li>Quinta letra</li>
</ol>
```

---

## **3. Listas Aninhadas**

É possível criar listas dentro de outras listas, sejam desordenadas ou ordenadas.

### **Exemplo**
```html
<ul>
    <li>Item principal 1
        <ul>
            <li>Subitem 1.1</li>
            <li>Subitem 1.2</li>
        </ul>
    </li>
    <li>Item principal 2
        <ol>
            <li>Subitem 2.1</li>
            <li>Subitem 2.2</li>
        </ol>
    </li>
</ul>
```

---

## **Exemplo Completo de Listas**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Listas</title>
</head>
<body>
    <h1>Listas Desordenadas</h1>
    <ul style="list-style-type: square;">
        <li>Item com marcador quadrado</li>
        <li>Item com marcador quadrado</li>
    </ul>

    <h1>Listas Ordenadas</h1>
    <ol type="i" start="4">
        <li>Quarto item</li>
        <li>Quinto item</li>
    </ol>

    <h1>Listas Aninhadas</h1>
    <ul>
        <li>Item principal
            <ul style="list-style-type: circle;">
                <li>Subitem com marcador circular</li>
            </ul>
        </li>
    </ul>
</body>
</html>
```

---

Com essas opções, você pode criar listas personalizadas para diferentes finalidades no seu site!
