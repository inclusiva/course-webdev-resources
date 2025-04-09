# **Aula 5: Seletores CSS e Hierarquia**

## 🌐 **O Poder dos Seletores CSS**

CSS oferece múltiplas formas de selecionar elementos. Veja o panorama:

```ASCII
SELETORES CSS
├── BÁSICOS
│   ├── Elemento (p, div)
│   ├── Classe (.destaque)
│   └── ID (#menu)
│
├── COMBINADORES
│   ├── Descendente (div p)
│   ├── Filho direto (ul > li)
│   └── Irmão adjacente (h1 + p)
│
└── PSEUDO-CLASSES
    ├── Estado (:hover, :focus)
    └── Posição (:nth-child)
```

## 🎯 **Objetivos da Aula**

- Dominar seletores básicos e combinadores
- Entender especificidade e cascata
- Aplicar pseudo-classes para interatividade
- Criar estilos condicionais eficientes

## 🧩 **Seletores Básicos na Prática**

### 1. Selecionando por Tipo

```css
/* Todos os parágrafos */
p {
    color: #333;
}
```

### 2. Selecionando por Classe

```css
/* Elementos com classe "destaque" */
.destaque {
    background: yellow;
}
```

### 3. Selecionando por ID

```css
/* Elemento com ID "cabecalho" */
#cabecalho {
    border-bottom: 2px solid;
}
```

## 🔍 **Hierarquia e Especificidade**

### Tabela de Peso dos Seletores

```ASCII
TIPO         EXEMPLO       ESPECIFICIDADE
──────────────────────────────────────
Inline       style="..."   1, 0, 0, 0
ID           #elemento     0, 1, 0, 0
Classe       .classe       0, 0, 1, 0
Elemento     p             0, 0, 0, 1
```

**Exemplo Prático:**

```css
#conteudo .destaque {
  /*
  ESPECIFICIDADE:  {
    ID: 0, 1, 0, 0
    Classe: 0, 0, 1, 0
  }
  ESPECIFICIDADE TOTAL: 0, 1, 1, 0
  */
    color: red;
}

.destaque {
    /*
  ESPECIFICIDADE:  {
    Classe: 0, 0, 1, 0
  }
  ESPECIFICIDADE TOTAL: 0, 0, 1, 0
  */
    color: blue; /* Perde para a regra acima por ser menos especifica. */
}
```

## 🛠 **Atividades Práticas**

### Atividade 1: Caça aos Seletores

```html
<div class="container">
    <header id="main-header">
        <h1>Título</h1>
        <nav class="menu-principal">
            <ul>
                <li><a href="#">Home</a></li>
                <li class="destaque"><a href="#">Sobre</a></li>
            </ul>
        </nav>
    </header>
</div>
```

**Desafios:**

1. Estilize apenas o link "Sobre" em vermelho
2. Adicione borda ao header sem afetar o container
3. Mude o fundo dos itens de lista pares

### Atividade 2: Formulário Interativo

```html
<form class="contato">
    <input type="text" placeholder="Nome" required>
    <input type="email" placeholder="E-mail">
    <button type="submit">Enviar</button>
</form>
```

**Exercícios:**

1. Estilize inputs obrigatórios diferentemente
2. Mude a cor do botão ao passar o mouse
3. Adicione ícone (::before) nos placeholders

## 💡 **Dicas**

1. **Evite IDs para estilos** - Use classes para reutilização
2. **Prefira especificidade baixa** - Facilita sobrescritas
3. **Organize seu CSS**:

   ```ASCII
   /* 1. Reset/Normalize */
   /* 2. Elementos base */
   /* 3. Componentes */
   /* 4. Helpers/Utilitários */
   ```

## 📚 **Recursos Complementares**

1. [Jogo CSS Diner](https://flukeout.github.io/) - Aprenda seletores brincando
2. [Specificity Calculator](https://specificity.keegan.st/) - Calcule pesos de seletores
3. [MDN Seletores CSS](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Selectors)
