# JavaScript

Chegámos ao último módulo de Web!
Já consegues criar uma página de um website com HTML e dar-lhes estilos com CSS.
Falta um pouco de funcionalidade e interatividade!

### Mas então o que é o JS?

 - Tecnologia web do lado do cliente (client-side scripting)
   - É uma linguagem de programação usada para programar o comportamento das páginas web, para as tornar dinâmicas!
 - Com JavaScript podemos:
   - Mudar o conteúdo de elementos HTML;
   - Mudar os atributos de elementos HTML;
   - Mudar os estilos dos elementos HTML (propriedades CSS);
   - Esconder/Mostrar elementos HTML;
   - ...

Apesar de com HTML e CSS escrevermos código, não lhes podemos chamar de linguagens de programação, são linguagens de markup e de estilos, respetivamente.
Já o JavaScript é uma linguagem de programação.

---

## Tag <script>

O código JavaScript pode ser incluído no <head> e/ou <body> dos documentos HTML.
Tem de ser inserido entre as tags <script> e </script>, como na imagem seguinte:

Exemplo de JS interno na ```<head>```
```html
<!DOCTYPE html>
<html>
  <head>
    <script>
      function mudaTexto() {
        document.getElementById("paragrafo1").innerHTML = “Escrevi outro texto.”;
      }
    </script>
  </head>
<body>
  <h1>A minha página</h1>
  <p id=“paragrafo1”>Um texto qualquer.</p>
  <button type=“button” onclick=“mudaTexto()”>Mudar o texto! </button>
</body>
</html>
```

Exemplo de JS interno no ```<body>```
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Exemplo</title>
  </head>
  <body>
    <h1>A minha página</h1>
    <p id=“paragrafo1">Um texto qualquer.</p>
    <button type="button" onclick=“mudaTexto()">Mudar o texto! </button>
    <script>
      function mudaTexto() {
        document.getElementById("paragrafo1").innerHTML = “Escrevi outro texto.";
      }
    </script>
  </body>
</html>
```

Alternativamente, pode ser escrito em ficheiros externos e referenciado no ficheiro HTML em questão.
Esta é normalmente a <b>melhor prática</b>.
À semelhança do CSS usamos a tag <link> para indicar qual é o nosso ficheiro de JS:

Ficheiro HTML index.html:
```html
<!DOCTYPE html>
<html>
  <body>
    <script src="ficheiro.js"></script>
  </body>
</html>
```
Ficheiro JavaScript index.js:
```js
function mudaTexto() {
   document.getElementById("paragrafo1").innerHTML = "Escrevi outro texto.";
}
```
- 💡 O ficheiro externo deve gravar-se com extensão .js.
- 💡 No ficheiro javascript externo não é necessário colocar as tags <script> e </script> a envolver o código.

---

## Output

Há quatro formas de o browser nos mostrar o output (resultado) de uma operação.

- ```alert("Hello world")```
- ```[elemento].write("Hello world")```
- ```[elemento].innerHTML = "Hello world"```
- ```console.log("Hello world")```

- alert()
Lança um aviso no topo da tua janela de browser com uma mensagem.
```html
<!DOCTYPE html>
<html>
  <body>
    <h1>A minha página</h1>

    <script>
      alert(“Olá a todos!”);
    </script>
  </body>
</html>
```

- [elemento].write()
Escreve texto no fundo do elemento escolhido. No exemplo abaixo o elemento foi o ```document```, logo escrevemos no fundo da página.
```html
<!DOCTYPE html>
<html>
  <body>

    <h1>A minha página</h1>

    <script>
      document.write(“<h2>O meu título</h2>”);
    </script>

  </body>
</html>
```

- [elemento].innerHTML
Escreve dentro de um elemento.
```html
<!DOCTYPE html>
<html>
  <body>
    <h1 id=“titulo”></h1>
    <script>
          document.getElementById("titulo").innerHTML = “A minha página fantástica!”;
    </script>
  </body>
</html>
```

- console.log()
Imprimir algo na consola do browser (temos de inspecionar a página, com a tecla F12 ou botão direito do rato, para ver a consola).
```html
<!DOCTYPE html>
<html>
  <body>
    <script>
      console.log(“Imprimir algo”);
    </script>
  </body>
</html>
```

---

## Comentários
```js
  // Comentário de apenas uma linha

  /* Comentário de várias linhas.
  Muito útil quando queremos adicionar
  muita informação nos comentários */
```

---

## Variáveis

Declaradas usando uma das palavras reservadas opcionais ```var``` e ```let```.

```js
  var x;
  var y, z;
  var a=2;
  var b=2, c=2;
  x=5;
  var c=a+b;
```

⚠️ O JavaScript é case-sensitive!
- x ≠ X
- lastname ≠ lastName

### Tipos de variáveis
```js
var a;                                         //undefined
var a=2;                                       //Número Inteiro (integer)
var a=2.67;                                    //Número Decimal (float)
var a=123e5;                                   //Notação Científica
var nome=“Zé Miguel”;                          //String (“”)
var nome=’João António’;                       //String (‘’)
var equipas=[“Benfica”, “Sporting”, “Porto”];  //Array
var pessoa={nome:”Miguel”, apelido:”Sousa”};   //Objecto
var a=true;                                    //Boolean
```

### Operações com variáveis
```js
// É possível declarar várias variáveis diferentes de uma só vez:
var a = 2, nome = “Zé Miguel”, carros = [“Volvo”, “Audi”];
```

```js
// É possível realizar operações aritméticas com variáveis em Javascript
var x = 5 + 2 + 3;  // 10
```

```js
// É possível “adicionar” strings: concatenação;
var x = “Maria” + “ “ + “Rita”;  // “Maria Rita”
```

```js
// Se um número for posto entre aspas, os seguintes são vistos como strings e concatenados:
var x = ”5” + 2 + 3;  // 523
var x = 2 + 3 + “5”;  // 55
```

### Operadores
- Operadores aritméticos
- Operadores de incremento e decremento
- Operadores de atribuição
- Operadores relacionais
- Operadores lógicos
- Operadores de cadeias (Strings)

| Operador | Descrição | Exemplo |
| ------------- |-------------|-------------|
| + | Adição | ```var x = 3, y = 2, z = x + y;  // z=5``` | 
| - | Subtração | ```var x = 3, y = 2, z = x - y;  // z=1``` |
| * | Multiplicação | ```var x = 3, y = 2, z = x * y;  // z=6``` |   
| / | Divisão | ```var x = 3, y = 2, z = x / y;  // z=1.5``` |
| % | Resto da divisão inteira | ```var x = 3, y = 2, z = x % y;  // z=1``` |

### Operadores de incremento e decremento

| Operador | Descrição | Exemplo |
| ------------- |-------------|-------------|
| ++ | Incremento | ```var x = 5; x++; var z = x; // z=6``` | 
| -- | Decremento | ```var x = 5; x--; var z = x; // z=4``` |
