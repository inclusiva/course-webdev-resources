# **Aula 1: Fundamentos do HTML - Estrutura Essencial**

## 🎯 **Objetivos da Aula:**

- Compreender o papel do HTML na web moderna
- Dominar a anatomia básica de um documento HTML
- Praticar com as principais tags de conteúdo
- Preparar a base para as aulas de semântica (Aula 2) e CSS

## 🌐 **O Que é HTML?**

HTML é a **linguagem de marcação padrão** para criar páginas web. Pense nele como:

```ASCII
HTML
├── Estrutura
│   ├── <html>
│   ├── <head>
│   └── <body>
├── Conteúdo
│   ├── Texto
│   └── Mídia
└── Conexões
    ├── <a>
    └── <nav>
```

**3 Pilares Fundamentais:**

1. **Hipertexto**: Ligações entre documentos
2. **Marcação**: Tags que definem elementos
3. **Linguagem**: Padrão universal para browsers

## 🧩 **Anatomia de um Documento HTML**

### 1. **Declaração DOCTYPE**

```html
<!DOCTYPE html>
```

- **O que faz**: Ativa o modo padrão do HTML5
- **Curiosidade**: Em versões antigas era bem mais complexo!

### 2. **Elemento (`<html>`)**

```html
<html lang="pt-BR">
</html>
```

- **Atributo essencial**: `lang` para acessibilidade e SEO
- **Dica**: Sempre feche suas tags!

### 3. **Elemento (`<head>`)**

```html
<head>
    <meta charset="UTF-8">
    <title>Minha Página</title>
    <meta name="viewport" content="width=device-width">
</head>
```

**Por que importa?**

- `charset`: Evita caracteres quebrados
- `viewport`: Essencial para mobile
- `title`: Aparece nos resultados de busca

### 4. **Elemento (`<body>`)**

```html
<body>
    <h1>Título Principal</h1>
    <p>Texto com <strong>ênfase</strong>.</p>
    <img src="logo.png" alt="Nosso Logo">
</body>
```

## 🛠 **Mãos na Massa: Primeiro Página HTML**

**Desafio Guiado:**

1. Crie `index.html`
2. Adicione estrutura básica
3. Insira:
   - Título principal
   - 1 parágrafo
   - 1 imagem (use placeholder)
   - 1 link para o MDN

**Template Inicial:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width">
    <title>Meu Primeiro Site</title>
</head>
<body>
    <!-- Conteúdo aqui -->
</body>
</html>
```

## 🔍 **Explorando Atributos**

**Tabela de Atributos Essenciais:**

| Atributo | Uso Típico | Exemplo |
|----------|------------|---------|
| `id` | Identificador único | `id="cabecalho"` |
| `class` | Estilização CSS | `class="destaque"` |
| `src` | Origem de mídia | `src="foto.jpg"` |
| `alt` | Texto alternativo | `alt="Foto de paisagem"` |
| `href` | Links | `href="https://site.com"` |

**Template Inicial:**

```html
<img src="https://via.placeholder.com/150"
     alt="Placeholder 150x150"
     id="logo-principal"
     class="borda-redonda">
```

## 🎮 **Desafios Interativos**

**Nível 1 - Básico:**
Complete o código:

```html
<p>Visite o site da <a href="_____">MDN</a>.</p>
```

**Nível 2 - Intermediário:**
Crie uma estrutura com:

- Título h1
- Parágrafo com palavra em negrito
- Imagem com texto alternativo

**Nível 3 - Avançado:**
Transforme isto:

```html
<div>Meu Texto</div>
```

Numa estrutura HTML5 válida com head e body completos

## 📚 **Recursos Complementares**

1. [Validador HTML do W3C](https://validator.w3.org/)
2. [HTML Living Standard](https://html.spec.whatwg.org/)
3. [Emmet Cheat Sheet](https://docs.emmet.io/cheat-sheet/) (para agilizar codificação)

## 💡 **Dicas**

Use sempre o atalho `!` + TAB no VS Code para gerar a estrutura básica automaticamente!"

**Tarefa de Casa:**
Crie uma página "Sobre Mim" com:

1. Título principal
2. 3 parágrafos
3. 1 imagem sua (ou placeholder)
4. Links para redes sociais

Envie como arquivo .zip ou compartilhe no CodePen!
