Há vezes em que queremos validar grupos de caracteres em uma expressão regular. É possível fazê-lo usando parênteses: `()`.

Você pode usar a expressão regular `/P(engu|umpk)in/g` para encontrar tanto `Penguin` quanto `Pumpkin` em uma string.

Depois é só usar o método `test()` para verificar se os grupos estão presentes na string.

```js
let testStr = "Pumpkin";
let testRegex = /P(engu|umpk)in/;
testRegex.test(testStr);
```

O método `test` retorna `true` aqui.

---

Corrija a regex para que ela valide os nomes `Franklin Roosevelt` e `Eleanor Roosevelt` levando em conta maiúsculas e minúsculas. A regex também deve permitir nomes do meio.

Depois corrija o código, fazendo com que a regex seja testada na string `myString`, retornando `true` ou `false`.

```let myString = "Eleanor Roosevelt";

let myRegex = /(Franklin|Eleanor) (([A-Z]\.?|[A-Z][a-z]+) )?Roosevelt/; // Altere esta linha

let result = myRegex.test(myString); // Altere esta linha

// Depois de passar no experimento do desafio com myString e ver como o agrupamento funciona