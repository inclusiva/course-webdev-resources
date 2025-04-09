# **Aula 6: CSS: Responsividade, Flexbox e Grid**

## 🌐 **O Mundo dos Layouts Modernos**

```ASCII
LAYOUTS CSS
├── FLEXBOX
│   ├── Alinhamento inteligente
│   └── Distribuição de espaço
│
├── GRID
│   ├── Grades precisas
│   └── Controle bidimensional
│
└── RESPONSIVO
    ├── Media Queries
    └── Unidades flexíveis
```

## 🎯 **Objetivos da Aula**

- Dominar Flexbox para layouts unidimensionais
- Criar estruturas complexas com CSS Grid
- Implementar designs responsivos
- Animar elementos com transições CSS

## 🧩 **Flexbox na Prática**

### Container Flex Básico

```css
.container {
    display: flex;
    justify-content: center; /* Alinhamento horizontal */
    align-items: center;    /* Alinhamento vertical */
    gap: 20px;             /* Espaço entre itens */
}
```

### Propriedades-Chave

```ASCII
flex-direction:  Direção (row/column)
flex-wrap:      Quebra de linha
flex-grow:      Distribuição de espaço
order:          Ordem visual
```

## 🔍 **CSS Grid Essencial**

### Grid Básico (2x2)

```css
.grid-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 100px auto;
    gap: 15px;
}
```

### Áreas Nomeadas

```css
.grid {
    grid-template-areas:
        "header header"
        "sidebar content";
}
.header { grid-area: header; }
```

## 📱 **Responsividade com Media Queries**

### Breakpoints Comuns

```css
/* Mobile */
@media (max-width: 600px) {
    .container { flex-direction: column; }
}

/* Tablet */
@media (min-width: 601px) and (max-width: 900px) {
    .grid { grid-template-columns: 1fr; }
}
```

## ✨ **Animações Suaves**

### Transição Básica

```css
.botao {
    transition: all 0.3s ease;
    background: blue;
}
.botao:hover {
    background: darkblue;
    transform: scale(1.05);
}
```

## 🛠 **Atividades Práticas**

### Desafio 1: Galeria Flexbox

```html
<div class="galeria">
    <img src="img1.jpg">
    <img src="img2.jpg">
    <!-- +3 imagens -->
</div>
```

**Tarefas:**

1. Crie layout responsivo que:
   - Mostre 3 colunas em desktop
   - 2 colunas em tablet
   - 1 coluna em mobile

### Desafio 2: Layout Completo

```html
<body>
    <header></header>
    <main></main>
    <aside></aside>
    <footer></footer>
</body>
```

**Requisitos:**

- Use Grid para áreas nomeadas
- Flexbox para o menu no header
- Animações nos links

## 💡 **Dicas**

1. **Mobile First**: Comece pelo mobile e adicione breakpoints
2. **Variáveis CSS**: Use `:root` para cores e espaçamentos
3. **DevTools**: Experimente layouts direto no navegador

## 📚 **Recursos Essenciais**

1. [Flexbox Froggy](https://flexboxfroggy.com/) - Jogo interativo
2. [CSS Grid Generator](https://cssgrid-generator.netlify.app/)
3. [Can I Use](https://caniuse.com/) - Suporte a recursos
