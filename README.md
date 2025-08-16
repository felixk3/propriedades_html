# Guia Rápido – HTML, CSS e JavaScript

## HTML (Estrutura da página)

### Estrutura básica

* `<!DOCTYPE html>` → Define o tipo de documento.
* `<html>` → Elemento raiz.
* `<head>` → Contém metadados (não aparece na página).
* `<body>` → Conteúdo visível da página.

### Elementos comuns

* `<h1> ... <h6>` → Títulos (h1 é o maior, h6 o menor).
* `<p>` → Parágrafo de texto.
* `<a href="url">` → Link para outra página.
* `<img src="imagem.jpg" alt="texto">` → Inserir imagem.
* `<ul>` → Lista não ordenada (bolinhas).
* `<ol>` → Lista ordenada (números).
* `<li>` → Item da lista.
* `<div>` → Container genérico.
* `<span>` → Container inline (usado para pequenos trechos).
* `<form>` → Formulário.
* `<input>` → Campo de entrada (texto, senha, etc.).
* `<button>` → Botão clicável.

---

## CSS (Estilo da página)

CSS define a **aparência** e **layout** do conteúdo.

### Seletores

* `tag { }` → Seleciona todas as tags.
* `.classe { }` → Seleciona elementos com a classe.
* `#id { }` → Seleciona elemento com id único.

### Propriedades principais

* **Cores e textos**

  * `color` → Cor do texto.
  * `background-color` → Cor de fundo.
  * `background: rgba(0, 0, 0, 0.5) url("imagem.jpg") no-repeat center/cover;` → Imagem com opacidade
  * `background-blend-mode: multiply;`→ Mistura a cor do background com a imagem do backgrond so assim funciona o efeito → Imagem com opacidade
  * `font-size` → Tamanho da fonte.
  * `font-family` → Tipo de letra.
  * `text-align` → Alinhamento do texto (left, center, right).
  * `font-weight` → Espessura da fonte (bold, normal).

* **Caixas**

  * `width` / `height` → Largura e altura.
  * `margin` → Espaço externo.
  * `padding` → Espaço interno.
  * `border` → Borda (largura, estilo, cor).
  * `border-radius` → Cantos arredondados.

* **Layout**

  * `display` → Como o elemento se comporta (block, inline, flex).
  * `flex` → Usado para criar layouts flexíveis.
  * `justify-content` → Alinhamento horizontal em flexbox.
  * `align-items` → Alinhamento vertical em flexbox.

* **Efeitos**

  * `hover` → Efeito ao passar o mouse.
  * `transition` → Animação suave de mudanças.
  * `box-shadow` → Sombra em elementos.

---

## JavaScript (Interatividade)

JavaScript adiciona **dinâmica** e **funcionalidades** à página.

### Conceitos básicos

* **Variáveis**

  * `let` → Variável que pode mudar.
  * `const` → Variável constante (não muda).
  * `var` → Variável antiga (evitar usar).

* **Tipos de dados**

  * `string` → Texto.
  * `number` → Números.
  * `boolean` → Verdadeiro ou falso.
  * `array` → Lista de valores.
  * `object` → Estrutura com pares chave\:valor.

* **Operadores**

  * `+ - * / %` → Operações matemáticas.
  * `==` → Igualdade (sem tipo).
  * `===` → Igualdade estrita (mesmo valor e tipo).
  * `&&` → E (and).
  * `||` → Ou (or).
  * `!` → Negação.

* **Estruturas de controle**

  * `if ... else` → Condições.
  * `for` → Loop definido.
  * `while` → Loop enquanto verdadeiro.

* **Funções**

  * `function nome() { }` → Bloco de código reutilizável.

* **Manipulação da página (DOM)**

  * `document.getElementById("id")` → Seleciona elemento pelo ID.
  * `document.querySelector("seletor")` → Seleciona pelo seletor CSS.
  * `element.innerHTML` → Altera conteúdo.
  * `element.style.property` → Altera estilo.
  * `addEventListener("click", funcao)` → Executa algo quando clicar.

---

## Exemplo de `for` no JavaScript

```js
// Mostra os números de 1 a 5
for (let i = 1; i <= 5; i++) {
  console.log("Número: " + i);
}
```

Saída no console:

```
Número: 1
Número: 2
Número: 3
Número: 4
Número: 5
```

---

## Exemplo de `while` no JavaScript

```js
// Conta até 5 usando while
let contador = 1;

while (contador <= 5) {
  console.log("Contador: " + contador);
  contador++;
}
```

Saída no console:

```
Contador: 1
Contador: 2
Contador: 3
Contador: 4
Contador: 5
```

---

## Exemplo de `element.style.property`

```html
<button id="meuBotao">Clique aqui</button>

<script>
  const botao = document.getElementById("meuBotao");

  botao.addEventListener("click", function() {
    botao.style.backgroundColor = "red";   // muda cor de fundo
    botao.style.color = "white";           // muda cor do texto
    botao.style.fontSize = "20px";         // aumenta o tamanho da letra
  });
</script>
```


## Exemplo de Objectos Em javascript e uso
```
  <script>
    // Nosso "dicionário" (mini banco de dados)
    const livros = {
      "javascript moderno": {
        autor: "Felix Khoza",
        ano: 2025,
        descricao: "Um guia prático de JavaScript moderno."
      },
      "html e css": {
        autor: "Nome do autor",
        ano: 2022,
        descricao: "Aprenda a criar páginas web responsivas do zero."
      },
      "algoritmos basicos": {
        autor: "N. Autor",
        ano: 2021,
        descricao: "Fundamentos de lógica e algoritmos para iniciantes."
      }
    };

    function buscar() {
      const entrada = document.getElementById("pesquisa").value.toLowerCase();
      const resultadoDiv = document.getElementById("resultado");

      if (livros[entrada]) {
        const livro = livros[entrada];
        resultadoDiv.innerHTML = `
          <h3>${entrada.toUpperCase()}</h3>
          <p><b>Autor:</b> ${livro.autor}</p>
          <p><b>Ano:</b> ${livro.ano}</p>
          <p><b>Descrição:</b> ${livro.descricao}</p>
        `;
      } else {
        resultadoDiv.innerHTML = `<p>Livro não encontrado.</p>`;
      }
    }
  </script>
```
