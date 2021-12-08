# <img alt="JavaScript logo" src="https://imgr.search.brave.com/u2mh-cKPyTuFQ3InY4b5uo_I6_XvT-o_8f6pKvJ4oYo/fit/1052/1052/ce/1/aHR0cDovLzMuYnAu/YmxvZ3Nwb3QuY29t/Ly1QVHR5M0NmVEdu/QS9UcFpPRWpUUV9X/SS9BQUFBQUFBQUFl/by9LZUt0X0Q1WDJ4/by9zMTYwMC9qcy5q/cGc" width=30 /> JavaScript

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

### Operadores de atribuição

| Operador | Exemplo | Equivale a |
| ------------- |-------------|-------------|
| = | ```x = y``` | ```x = y``` | 
| += | ```x += y``` | ```x = x + y``` |
| -= | ```x -= y``` | ```x = x - y``` |
| *= | ```x *= y``` | ```x = x * y``` |
| /= | ```x /= y``` | ```x = x / y``` |
| %= | ```x %= y``` | ```x = x % y``` |
 
 ### Operadores relacionais
 
| Operador | Descrição | Exemplo |
| ------------- |-------------|-------------|
| == | ```Igual a``` | ```2 == 1 //false``` |
| != | ```Diferente de``` | ```2 != 1 //true``` |
| > | ```Maior do que``` | ```2 > 1 // true``` |
| < | ```Menor do que``` | ```2 < 1 //false``` |
| >= | ```Maior ou igual a``` | ```2 >= 1 //true``` |
| <= | ```Menor ou igual a``` | ```2 <= 1 //false``` |
 
### Operadores lógicos
 
| Operador | Descrição | Exemplo |
| ------------- |-------------|-------------|
| ! | ```Negação``` | ```x = 2; y = 1; !(x==y); //false``` |
| && | ```Conjunção``` | ```x = 1; y = 5; (x<3 && y<3); //false``` |
| || | ```Disjunção``` | ```x = 1; y = 5; (x<3 || y<3); //true``` |
 
### Operadores de cadeias (strings)
 
| Operador | Descrição | Exemplo |
| ------------- |-------------|-------------|
| + | ```Concatenação``` | ```string1 = "Bom"; string2 = " dia"; stringFinal = string1 + string2; // "Bom dia"``` |

---
 
## Exercício 🏋️‍♀️

A consola do navegador de internet consegue ler e correr JavaScript!
Adeus à calculadora!
Olá consola! 😂
Testa os diferentes tipos de variáveis e operadores lá.
 
 ---

### Instruções condicionais
 
Em JavaScript definem-se as seguintes instruções condicionais:
- if
- else
- else if
- switch-case 
 
### if
 
```js
if (trueOrFalse) {
    // código a ser executado caso a condição seja verdadeira
}
```

```js
if (idade < 5) {
    mensagem = “Ainda és um bebé”;
}
 ```
 
### else
 
```js
if (trueOrFalse) {
    // código a ser executado caso a condição seja verdadeira
} else {
	// código a ser executado caso a condição seja falsa
}
```
 
```js
if (idade < 5) {
    mensagem = “Ainda é um bebé";
} else {
    mensagem = “Já não és nenhum bebé";
}
```

### else if

```js
if (condição1) {
    // código a ser executado caso a condição1 seja verdadeira
} else if (condição2){
	// código a ser executado caso a condição1 seja falsa e a condição2 seja verdadeira
} else {
	// código a ser executado caso ambas as condições sejam falsas
}
```
 
```js
if (idade < 5) {
    mensagem = “Ainda é um bebé";
} else if (idade < 18) {
    mensagem = “És um adolescente";
} else {
    mensagem = “És um adulto!”;
}
```
 
### switch
			  
```js
switch(expressão) {
    case n:
        // bloco de código
        break;
    case n:
        // bloco de código
        break;
    default:
        // bloco de código default
}
```
			  
```js
var diaSemana = 1;

switch (diaSemana) {
    case 1:
        dia = "Segunda";
        break;
    case 2:
        day = "Terça";
        break;
    default:
        day = "Outro";
}
```

Caso nenhum valor dos case coincida com o valor da expressão utilizada no switch é corrido o bloco de código no ```default```.
			  
			  
			  
			  
###

```js
			  
```
[GitHub Pages](https://pages.github.com/)
![githubpages1](https://user-images.githubusercontent.com/39055313/135725380-daf77fad-08ee-4013-945b-47469510fa61.jpeg)
