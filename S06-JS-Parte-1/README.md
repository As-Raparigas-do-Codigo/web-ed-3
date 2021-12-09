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

<details>
<summary>Tag \<script\> </summary>

wda
</details>
## Tag \<script\>

O código JavaScript pode ser incluído no <head> e/ou <body> dos documentos HTML.
Tem de ser inserido entre as tags <script> e </script>, como na imagem seguinte:

Exemplo de JS interno na ```<head>```
```html
<!DOCTYPE html>
<html>
  <head>
    <script>
      function mudaTexto() {
        document.getElementById("paragrafo1").innerHTML = "Escrevi outro texto.";
      }
    </script>
  </head>
<body>
  <h1>A minha página</h1>
  <p id="paragrafo1">Um texto qualquer.</p>
  <button type="button" onclick="mudaTexto()">Mudar o texto! </button>
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
    <p id="paragrafo1">Um texto qualquer.</p>
    <button type="button" onclick="mudaTexto()">Mudar o texto! </button>
    <script>
      function mudaTexto() {
        document.getElementById("paragrafo1").innerHTML = "Escrevi outro texto.";
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
      alert("Olá a todos!");
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
      document.write("<h2>O meu título</h2>");
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
    <h1 id="titulo"></h1>
    <script>
          document.getElementById("titulo").innerHTML = "A minha página fantástica!";
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
      console.log("Imprimir algo");
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
var nome="Zé Miguel";                          //String ("")
var nome=’João António’;                       //String (‘’)
var equipas=["Benfica", "Sporting", "Porto"];  //Array
var pessoa={nome:"Miguel", apelido:"Sousa"};   //Objecto
var a=true;                                    //Boolean
```

### Operações com variáveis
```js
// É possível declarar várias variáveis diferentes de uma só vez:
var a = 2, nome = "Zé Miguel", carros = ["Volvo", "Audi"];
```

```js
// É possível realizar operações aritméticas com variáveis em Javascript
var x = 5 + 2 + 3;  // 10
```

```js
// É possível "adicionar" strings: concatenação;
var x = "Maria" + " " + "Rita";  // "Maria Rita"
```

```js
// Se um número for posto entre aspas, os seguintes são vistos como strings e concatenados:
var x = "5" + 2 + 3;  // 523
var x = 2 + 3 + "5";  // 55
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
| == | Igual a | ```2 == 1 //false``` |
| != | Diferente de | ```2 != 1 //true``` |
| > | Maior do que | ```2 > 1 // true``` |
| < | Menor do que | ```2 < 1 //false``` |
| >= | Maior ou igual a | ```2 >= 1 //true``` |
| <= | Menor ou igual a | ```2 <= 1 //false``` |
 
### Operadores lógicos
 
| Operador | Descrição | Exemplo |
| ------------- |-------------|-------------|
| ! | Negação | ```x = 2; y = 1; !(x==y); //false``` |
| && | Conjunção | ```x = 1; y = 5; (x<3 && y<3); //false``` |
| || | Disjunção | ```x = 1; y = 5; (x<3 || y<3); //true``` |
 
### Operadores de cadeias (strings)
 
| Operador | Descrição | Exemplo |
| ------------- |-------------|-------------|
| + | Concatenação | ``` "Bom"; string2 = " dia"; stringFinal = string1 + string2; // "Bom dia"``` |

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
    mensagem = "Ainda és um bebé";
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
    mensagem = "Ainda é um bebé";
} else {
    mensagem = "Já não és nenhum bebé";
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
    mensagem = "Ainda é um bebé";
} else if (idade < 18) {
    mensagem = "És um adolescente";
} else {
    mensagem = "És um adulto!";
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

---

### Instruções iterativas
 
Em Javascript definem-se as seguintes instruções iterativas:
- for
- while  
			  
### O ciclo for
 
```js
for (start; end; step) {
    // código a ser executado 
}
```

```js
for (var i = 1; i < 5; i++) {
    document.write("Número: " + i + "<br>");
}
```

```js
var dias = ["Seg", "Ter", "Qua", "Qui", "Sex"];
for (var i = 0; i < 5; i++) {
    alert(dias[i]);
}
```

### O ciclo while
 
```js
while (condição) {
    // código a ser executado
}
```

```js
var i = 0;
while (i < 5) {
    document.write("Número: " + i + "<br>");
    i++;
}
```
Não esquecer de incrementar/decrementar/alterar a variável, caso o contrário o loop nunca vai parar! (crasha o browser)

---

### Instruções break e continue

### break

A instrução break interrompe um ciclo passando o controlo à primeira instrução a seguir ao ciclo.

```js
for (i = 0; i < 5; i++) {
    if (i == 3) {
      break;
    }
  document.write("Número: " + i + "<br>");
}
document.write("Terminei!");
```

### continue

A instrução continue interrompe o ciclo passando para iteração seguinte.

```js
for (i = 0; i < 5; i++) {
  if (i == 3) {
    continue; 
  }
   document.write("Número: " + i + "<br>");
}
document.write("Terminei!");
```

---
### Funções

Uma função é uma sequência de instruções com o objectivo de desempenhar uma tarefa específica.

- Pode ser invocada em qualquer ponto do programa, e quando é invocada (chamada), ela executa essas instruções.
- O Javascript tem algumas funções predefinidas, mas nós podemos criar as nossas.
- As funções têm argumentos que são passados  na chamada da função e usados pela função como variáveis locais.
- As funções podem devolver um valor ao programa de chamada mediante a utilização da instrução return.

### Funções predefinidas do javascript (STRINGS)

| Função | Descrição | Exemplo |
| ------------- |-------------|-------------|
| length() | Número de caracteres | ```"Ola".length  //3``` | 
| concat() | Concatenação | ```"Ola".concat(" pessoas"); //"Ola pessoas"``` |
| toUpperCase() | Maiúsculas | ```"Ola".toUpperCase(); //"OLA"``` |   
| toLowerCase() | Minúsculas | ```"Ola".toLowerCase(); //"ola"``` |
| charAt(i) | Caracter na posição i | ```"Ola".charAt(2); //"a"``` |
| indexOf(char) | Posição do caracter char | ```"Ola".indexOf(‘O’); //0 (-1 se não existir) ``` |
| substring(inicio, final) | Extrai string entre os indices início e final | ```"Palavra".substring(2,4); //la``` | 
| split(separador) | Separa as strings pelo separador e converte-os num array | ```"Ola".concat(" pessoas"); //"Ola pessoas"```  |
| | |```var letras = "Ola".split(""); // letras = ["O", "l", "a"];```|


### Funções predefinidas do javascript (ARRAYS)

| Função | Descrição | Exemplo |
| ------------- |-------------|-------------|
| length() | Número de elementos | ```[1,2,3,4].length; //4``` | 
| concat() | Concatenação | ```[1,2,3,4].concat([5,6]); //[1,2,3,4,5,6]``` |
| join(separador) | Une elementos por separador, formando uma string | ```var array = ["Ola", "amigos"]; var msg = array.join(""); //"Olaamigos"var msg = array.join(" "); //"Ola amigos" ``` |   
| pop() | Retira o último elemento do array e devolve-o | ```var array = [1,2,3,4]; var ultimo = array.pop(); //ultimo = 3, array = [1,2,3]``` |
| push() | Adiciona um elemento no fim do array | ```var array = [1,2,3,4]; array.push(5); //array = [1,2,3,4,5]``` | 
| shift() | Retira o primeiro elemento do array e devolve-o | ```var array = [1,2,3,4]; var primeiro = array.shift(); //primeiro = 1, array = [2,3,4]``` |
| unshift() | Adiciona um elemento ao início do array | ```var array = [1,2,3,4]; array.unshift(0); //array = [0,1,2,3,4] ``` |   
| reverse() | Inverte a ordem dos elementos do array | ```var array = [1,2,3,4]; array.reverse(); //array = [4,3,2,1]``` |

### Funções predefinidas do javascript (NÚMEROS)


| Função | Descrição | Exemplo |
| ------------- |-------------|-------------|
| isNaN() | Verifica se um valor é um número ilegal (Not-a-Number) | ```isNaN(123); //false isNaN(0/0); //true``` | 
| toFixed(n) | Converte o número numa string apenas com n casas decimais | ```var numero1 = 123.3456; var numero2 = toFixed(numero1); //numero2 = "123"``` |
| parseFloat() | Faz o parse de uma string e devolve um float | ```var a = parseFloat("10.33"); //a = 10.33;``` |   
| parseInt() | Faz o parse de uma string e devolve um integer | ```var a = parseInt("10.33"); //a = 10;``` |


### Criação e invocação de funções

```js
function nome_função(parametro1, parametro2, parametro3, ...) {
   // código a ser executado 
}
```

```js
function soma(a, b) {
    return a + b;             
}
var x = soma(3,2);
```


### Criação de funções (RETURN)

As funções param de executar assim que surgir a expressão return ("voltar", "devolver").
Uma função pode ou não ter return.


```js
function soma(a, b) {
    return a + b;             
}
var x = soma(3,2);  // x = 5
document.write("O valor de x é: " + x);
```


### Eventos

O Javascript é uma linguagem orientada a eventos.

Os eventos podem ser produzidos pelo sistema (e.g. load de uma página web) ou resultar de acções directas do utilizador (e.g. premir um botão).

Com Javascript podemos "reagir" a esses eventos: despoletar acções (executar código) quando esses eventos ocorrem.


### Resposta a eventos de sistema (EXEMPLO)

```js
<!DOCTYPE html>
<html>
<head>
<script>
function entrar() {
    alert("Bem-vindo à nossa página");  
}
</script>

<body onload="entrar();">
<h1>A nossa página</h1>
</body>
</html>
```

### Resposta a eventos de utilizadores (EXEMPLO)

```js
<!DOCTYPE html>
<html>
<head>
<script>
  function mostraMsg() {
    alert("Uma mensagem para ti!");  
  }
</script>

<body>
<button onclick="mostraMsg();">
  Clica para veres uma mensagem
</button>
</body>
</html>
```

### Eventos Comuns


| Evento | Descrição | Elementos para os quais está definido |
| ------------- |-------------|-------------|
| onclick | Clicar num elemento | Todos os elementos | 
| onmouseover | O cursor "entra" num elemento | Todos os elementos |
| onmouseout | O cursor "sai" de uma elemento | Todos os elementos |   
| onchange | Desselecionar um elemento que se modificou entretanto | ```<input>, <select>, <textarea>``` |
| onkeypress | Clicar num tecla | Elementos de formulario e ```<body>``` |
| onload | Quando o browser carrega a página | ```<body>``` |   

Existem imensos outros eventos. Consultar: http://www.w3schools.com/jsref/dom_obj_event.asp



### Exercícios

## Exercício 1 🏋️‍♀️

Verifica o texto inserido pelo utilizador na caixa de texto mensagem e imprima-o quando o utlizador prime o botão. Testa as diferentes formas de output para imprimir:
- ```alert()```
- ```[elemento].write()```
- ```[elemento].innerHTML```
- ```console.log()```

```js
<!DOCTYPE html>
<html>
  <body>
    <h1 id="titulo"><h1/>
    <form>
      <input type="text" id="mensagem"/>
      <input type="button"onClick="mostrarMensagem()" value="Clica-me" />
    </form>
    <script>
      function mostrarMensagem() {
        // completar
      }
    </script>
  </body>
</html>
```

## Exercício 2 🏋️‍♀️

Para que o código fique mais claro, experimenta guardar o texto numa variável e usa a mesma variável para todas as formas de output.

## Exercício 3 🏋️‍♀️

Vamos adicionar uma validação ao nosso exercício anterior:
- Alerta o utilizador se a caixa de texto estiver vazia!
- Senão altera o título com a mensagem introduzida
- Dicas: usar ```if``` e ```else```

## Exercício 4 🏋️‍♀️

Vamos adicionar uma validação ao nosso exercício anterior:
- Alerta o utilizador se a caixa de texto estiver vazia!
- Senão altera o título com a mensagem introduzida
- Dicas: usar ```if``` e ```else```

## Exercício 5 🏋️‍♀️

- Escreva uma função calculaArea() que receba como argumento o raio de uma circunferência e retorne o valor da sua área (área = π x r^2). 
- Crie um ciclo for que imprima para a consola as áreas de círculos com raios de 2 a 9, sendo que no caso do raio ser 3, o ciclo deve saltar essa iteração.



### 
```js
			  
```
[GitHub Pages](https://pages.github.com/)
![githubpages1](https://user-images.githubusercontent.com/39055313/135725380-daf77fad-08ee-4013-945b-47469510fa61.jpeg)
