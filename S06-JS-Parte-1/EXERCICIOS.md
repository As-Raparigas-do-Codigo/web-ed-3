# Exercícios 🏋️‍♀️

Hora de pôr tudo em prática!

<details>
<summary>Exercício 1</summary>

A consola do navegador de internet consegue ler e correr JavaScript!<br>
Adeus à calculadora!<br>
Olá consola! 😂<br>
Testa os diferentes tipos de variáveis e operadores lá.

</details>

<details>
<summary>Exercício 2</summary>

Verifica o texto inserido pelo utilizador na caixa de texto mensagem e imprime-o quando o utlizador prime o botão.<br>
Testa as diferentes formas de output para imprimir:
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
      <input type="button" id="button" onClick="mostrarMensagem()" value="Clica-me" />
    </form>
    <script>
      function mostrarMensagem() {
        // completar (Usa document.getElementById("button").value para aceder o valor do elemento)
      }
    </script>
  </body>
</html>
```
</details>

<details>
<summary>Exercício 3</summary>

Para que o código do exercício 2 fique mais claro, experimenta guardar o texto numa variável e usa a mesma variável para todas as formas de output.

</details>

<details>
<summary>Exercício 4</summary>

Vamos adicionar uma validação ao nosso exercício anterior:
- Alerta o utilizador se a caixa de texto estiver vazia.
- Senão estiver, altera o título com a mensagem introduzida
  
</details>

<details>
<summary>Exercício 5</summary>

Altera a função mostrarMensagem() para alertar uma mensagem da personagem dos Simpsons cujo nome foi introduzido na caixa de texto:
“bart” -> “Ay Caramba!”
“homer” -> “D’oh!!”
Adiciona uma mensagem padrão para personagens não reconhecidas

</details>

<details>
<summary>Exercício 6</summary>

- Escreva uma função calculaArea() que receba como argumento o raio de uma circunferência e retorne o valor da sua área (área = π x r^2). 
- Cria um ciclo ```for``` que imprima para a consola as áreas de círculos com raios de 2 a 9, sendo que no caso do raio ser 3, o ciclo deve saltar essa iteração.
  
Link útil: https://www.w3schools.com/jsref/jsref_pi.asp
  
</details>

  <details>
    <summary>Desafio da W3Schools</summary>
 https://www.w3schools.com/js/js_quiz.asp
  </details>
  
  
