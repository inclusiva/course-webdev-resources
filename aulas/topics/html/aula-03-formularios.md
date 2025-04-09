# **Aula 3: Tabelas e Formulários - Versão Integrada com Progressão para CSS**

## 🎯 **Objetivos da Aula**

- Construir tabelas semanticamente ricas para exibição de dados
- Criar formulários acessíveis com validação básica

## 🧩 **Parte 1: Tabelas**

### Estrutura Semântica

```html
<table>
  <caption>Horário de Aulas</caption>
  <colgroup>
    <col style="width: 20%">
    <col style="width: 80%">
  </colgroup>
  <thead>
    <tr>
      <th scope="col" aria-label="Horário">⏰</th>
      <th scope="col">Atividade</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td headers="horario">08:00</td>
      <td>Introdução ao HTML</td>
    </tr>
  </tbody>
</table>
```

## 📋 **Parte 2: Formulários**

### Estrutura Semântica

```html
<form id="form-login" class="formulario-padrao">
  <div class="campo-form">
    <label for="email" class="rotulo">E-mail</label>
    <input type="email" id="email" class="entrada-texto">
    <span class="dica">Ex: nome@provedor.com</span>
  </div>

  <button type="submit" class="botao-primario">
    <span class="icone">→</span> Enviar
  </button>
</form>
```

**Preparação para CSS:**

- Classes específicas para cada elemento
- Estrutura aninhada para seletores descendentes
- Elementos vazios para ícones e decoradores

## 🛠 **Atividade Prática**

**Desafio: Crie um sistema de reservas com:**

1. Tabela de horários disponíveis
2. Formulário de reserva contendo:
   - Seletores de data/horário
   - Campos de dados pessoais
   - Área de observações

**Template inicial:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Reservas</title>
</head>
<body>
    <section class="container">
        <h2>Faça sua reserva</h2>

        <!-- Tabela aqui -->

        <!-- Formulário aqui -->
    </section>
</body>
</html>
```

## 📚 **Recursos Complementares**

1. [MDN: Tabelas Acessíveis](https://developer.mozilla.org/pt-BR/docs/Learn/HTML/Tables/Advanced)
2. [HTML5 Form Validation](https://web.dev/learn/forms/validation/)
3. [Preview CSS para Formulários](https://codepen.io/collection/XJyNPm)

## 💡 **Dicas**

Use cores diferentes para `<th>` e `<td>` para melhor legibilidade - isso será refinado na Aula 4!

```html
<style>
/* Prévia do que virá */
th { background-color: #f3f3f3; }
td { background-color: #fff; }
</style>
```
