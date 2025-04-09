# **Aula 4: Introdução ao CSS**

## 🌐 **O Que é CSS?**

CSS (**Cascading Style Sheets**)  é a linguagem que dá vida e estilo às páginas web. Pense nele como:

```ASCII
CSS
├── ESTILOS VISUAIS
│   ├── Cores e fundos
│   ├── Tipografia
│   └── Modelo de caixa
├── CONTROLE
│   ├── Seletores
│   └── Cascata/herança
└── INTERAÇÃO
    ├── Efeitos visuais
    └── Adaptação a dispositivos
```

**3 Princípios Fundamentais:**

1. **CASCATA**: Ordem de aplicação das regras
2. **ESPECIFICIDADE**: Peso dos seletores
3. **HERANÇA**: Propriedades que se propagam

## 🧩 **Anatomia de uma Regra CSS**

### Estrutura Básica

```ASCII
[seletor] {
    [propriedade]: [valor];
    └── Declaração completa
}
```

**Exemplo Prático:**

```css
/* Seletor de elemento */
article {
    margin: 20px 0;    /* Declaração 1 */
    padding: 15px;      /* Declaração 2 */
    border: 1px solid;  /* Declaração 3 */
}
```

## 🖌️ **Métodos de Aplicação**

### Comparação Visual

```ASCII
MÉTODO          SINTAXE                      USO IDEAL
─────────────── ─────────────────────────── ────────────────────────
Inline          style="prop:valor;"         Ajustes pontuais
Interno         <style>...</style>          Páginas únicas
Externo         <link href="arquivo.css">   Projetos completos
```

**Fluxo Recomendado:**

```ASCII
HTML
│
├─▶ CSS Inline (Emergencial)
│
├─▶ CSS Interno (Protótipos)
│
└─▶ CSS Externo (Produção)
```

## 🎨 **Propriedades Fundamentais**

### Grupo 1: Tipografia

```ASCII
font-family: Define a família de fontes (ex: Arial, Times)
font-size:   Tamanho do texto (px, rem, em)
line-height: Espaço entre linhas (1.5 é o ideal para leitura)
text-align:  Alinhamento (left, center, right, justify)
font-weight: Espessura (normal, bold, 100-900)
```

### Grupo 2: Cores

```ASCII
color:        Cor do texto (hex, rgb, nome)
background:   Cor/fundo do elemento
opacity:      Transparência (0 a 1)
text-shadow:  Sombra no texto (horizontal vertical blur cor)
```

### Grupo 3: Modelo de Caixa (Box Model)

```ASCII
margin:       Espaço EXTERNO (top right bottom left)
padding:      Espaço INTERNO (mesma sintaxe que margin)
border:       Contorno (width style color)
width/height: Dimensões (px, %, vw/vh)
box-sizing:   Como calcular tamanhos (content-box/border-box)
```

## 🌟 Conceito Chave: "Modelo de Caixa" (Box Model)

```ASCII
CAIXA DE UM ELEMENTO
┌──────────────────────────────┐
│        margin (externo)      │
│   ┌──────────────────────┐   │
│   │     border           │   │
│   │   ┌──────────────┐   │   │
│   │   │  padding     │   │   │
│   │   │   ┌──────┐   │   │   │
│   │   │   │conteú│   │   │   │
│   │   │   │  do  │   │   │   │
│   │   │   └──────┘   │   │   │
│   │   └──────────────┘   │   │
│   └──────────────────────┘   │
└──────────────────────────────┘
```

### Entendendo box-sizing

```css
* {
    box-sizing: border-box;                     /* Mágica do layout previsível! */
}
```

#### **Por que isso importa?**

- content-box (padrão): padding e border **ACRESCENTAM** ao width

- border-box: padding e border **ESTÃO DENTRO** do width

#### **Exemplo:**

```html
<div class="caixa1">Caixa Normal</div>
<div class="caixa2">Caixa border-box</div>

<style>
    .caixa1, .caixa2 {
        width: 200px;
        padding: 20px;
        border: 5px solid;
    }

    .caixa2 {
        box-sizing: border-box;
    }
</style>
```

## 🧩 Por Que Normalizar o CSS?

Quando diferentes navegadores (Chrome, Firefox, Edge) exibem a mesma página, eles podem ter estilos padrão diferentes. A normalização ajuda a corrigir:

- Margens diferentes
- Tamanhos de fonte inconsistentes
- Espaçamentos desiguais

**Exemplo:**

```css
/* Remove margens e preenchimentos padrão */
* {
    margin: 0;
    padding: 0;
}

/* Padroniza o tamanho das caixas */
*,
*::before,
*::after {
    box-sizing: border-box;
}

/* Define fonte base */
body {
    font-family: Arial, sans-serif;
    font-size: 16px;
    line-height: 1.5;
}
```

## 🛠 **Atividades Práticas**

### **Atividade 1: Explorando o Box Model**

1. Crie um arquivo HTML com 3 divs
2. Estilize cada uma diferentemente:

   ```css
   .caixa-a {
       width: 200px;
       padding: 10px;
       border: 2px dashed red;
   }

   .caixa-b {
       width: 200px;
       padding: 20px;
       border: 5px dotted blue;
       box-sizing: border-box;
   }
   ```

3. Compare como o tamanho muda

### **Atividade 2: Normalização Básica**

1. Crie um arquivo `reset.css` com:

   ```css
   * {
       margin: 0;
       padding: 0;
       box-sizing: border-box;
   }

   body {
       font-family: Arial, sans-serif;
       line-height: 1.5;
   }
   ```

2. Aplique em uma página simples e observe:
   - Como os parágrafos ficam sem margem
   - Como os elementos se comportam de forma mais previsível

### **Atividade 3: Primeiro Estilo Completo**

1. Crie um novo arquivo HTML chamado cartao.html e faça a estilização da tag `<body>` utilizando das seguintes propriedades:
    - background-color
    - font-family
    - padding
2. Customize o Cartão:
    - Adicione estilos para as seguintes propriedades do elemento com a classe `.cartao`.
      - background
      - width
      - padding
      - border-radius
3. Efeitos visuais **(OPCIONAL)**:
   - Ex.: Adicione estilos para quando uma usuária passar o cursor do mouse no cartão.
   - Para adicionar estilos nesse caso usamos o seletor: `.cartao:hover`

**Template Inicial:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Meu Cartão</title>
    <style>
        /* SEU CSS VAI AQUI DENTRO */
    </style>
</head>
<body>
    <div class="cartao">
        <h2>Título do Cartão</h2>
        <p>Descrição ou conteúdo do cartão.</p>
    </div>
</body>
</html>
```

## 📚 **Recursos Complementares**

### **Tabela: box-sizing vs content-box**

```ASCII
CONFIGURAÇÃO      WIDTH: 200px + PADDING: 20px   RESULTADO
───────────────────────────────────────────────────────────
content-box       + 20px de cada lado           240px total
border-box        Inclui o padding              200px total
```

### **Glossário Simplificado**

```ASCII
MARGIN:    Espaço fora do elemento
BORDER:    Linha em volta do elemento
PADDING:   Espaço dentro, antes do conteúdo
WIDTH:     Largura do conteúdo (ou da caixa)
```

## 💡 **Dicas**

1. **Sempre comece com border-box** - facilita cálculos
2. **Use unidades relativas** como `rem` e `%` quando possível
3. **Inspecione elementos** com Ferramentas do Desenvolvedor (F12)
4. **Comece simples** - domine o box model antes de animações
