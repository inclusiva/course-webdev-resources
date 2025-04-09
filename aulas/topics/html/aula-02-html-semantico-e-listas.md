# **Aula 2: HTML Semântico e Listas**

## 🎯 **Objetivos da Aula:**

- Dominar o uso das tags semânticas do HTML5
- Criar menus de navegação eficientes
- Construir listas organizadas para diferentes propósitos
- Entender a importância da estrutura semântica para acessibilidade e SEO

## 🌐 **Por que isso importa?**

As tags semânticas são como placas de trânsito para:

- **Navegadores** entenderem seu conteúdo
- **Leitores de tela** para pessoas com deficiência visual
- **Mecanismos de busca** como Google para indexação

## 🧩 **Blocos de Construção Semântica**

### 1. **Elemento (`<header>`)**

```html
<header>
    <h1>Portal de Notícias Tech</h1>
    <p>As últimas novidades do mundo da tecnologia</p>
</header>
```

**O que faz:** Define o cabeçalho da página ou seção

### 2. **Elemento (`<nav>`)**

```html
<nav>
    <ul>
        <li><a href="#home">Início</a></li>
        <li><a href="#noticias">Notícias</a></li>
    </ul>
</nav>
```

**Dica:** Use para menus principais, nunca para links aleatórios

### 3. **Elemento (`<main>`)**

```html
<main>
    <article>
        <h2>Novo iPhone Lançado</h2>
        <p>Apple surpreende com novas funcionalidades...</p>
    </article>
</main>
```

**Regra de ouro:** Apenas UM `<main>` por página!

### 4. **Elemento (`<footer>`)**

```html
<footer>
    <p>© 2023 Portal Tech</p>
    <address>contato@portaltech.com</address>
</footer>
```

**Extra:** Ótimo para informações de copyright e contato

## 📋 **Criando Listas**

### Listas Não Ordenadas (Para itens sem hierarquia)

```html
<ul>
    <li>Mouse</li>
    <li>Teclado</li>
    <li>Monitor</li>
</ul>
```

**Uso ideal:** Menus, características, itens relacionados

### Listas Ordenadas (Para passos ou rankings)

```html
<ol>
    <li>Ligar o computador</li>
    <li>Inserir senha</li>
    <li>Abrir navegador</li>
</ol>
```

**Bônus:** Experimente `type="A"` ou `start="10"`

## 🛠 **Mãos na Massa: Vamos Construir!**

**Desafio Guiado:**

1. Crie um arquivo `blog.html`
2. Adicione a estrutura básica com `<!DOCTYPE html>`
3. Insira:
   - Cabeçalho com título e slogan
   - Menu com 3 seções
   - Área principal com 1 artigo
   - Rodapé com informação fictícia

**Template Inicial:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Meu Blog Tech</title>
</head>
<body>
    <!-- Seu código vem aqui! -->
</body>
</html>
```

## 🎮 **Desafio Interativo**

**Transforme isto:**

```html
<div>
    <div>1. Acordar</div>
    <div>2. Escovar os dentes</div>
</div>
```

**Nisto:**

```html
<ol>
    <li>Acordar</li>
    <li>Escovar os dentes</li>
    <!-- Adicione mais 3 itens da rotina matinal -->
</ol>
```

**Super Desafio:**
Crie uma lista não ordenada dentro do seu `<nav>` com ícones usando emojis:

```html
<li>🏠 Home</li>
<li>🔍 Buscar</li>
```

## 📚 **Recursos Complementares**

1. [MDN Semântica HTML](https://developer.mozilla.org/pt-BR/docs/Glossary/Semantics) - Guia completo
2. [W3Schools Listas HTML](https://www.w3schools.com/html/html_lists.asp) - Tutorial interativo
3. [HTML5 Doctor](http://html5doctor.com/) - Exemplos avançados

## 💡 **Dicas**

Tags semânticas são como organizar seu armário - quando tudo tem seu lugar certo, fica mais fácil para você e para os outros encontrarem o que precisam!

## 📝 **Tarefa para Casa**

Crie uma página "Receita de Bolo" usando:

- `<header>` para o título da receita
- `<section>` para ingredientes e modo de preparo
- `<ul>` para ingredientes
- `<ol>` para passos de preparo
- `<footer>` com dados fictícios do chef

Envie como arquivo `.html` ou compartilhe no CodePen!
