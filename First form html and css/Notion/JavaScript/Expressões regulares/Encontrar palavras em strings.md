Regular expressions are used in programming languages to match parts of strings. You create patterns to help you do that matching.

Se você quiser encontrar a palavra `the` na string `The dog chased the cat`, você poderia usar a seguinte expressão regular: `/the/`. Note que aspas não são necessárias ao redor da expressão regular.

O JavaScript oferece múltiplas maneiras de usar regexes. Uma dessas maneiras é com o método `.test()`. O método `.test()` aplica a regex à string dentro dos parênteses e retorna `true` caso encontre o padrão ou `false` caso contrário.

```js
let testStr = "freeCodeCamp";
let testRegex = /Code/;
testRegex.test(testStr);
```

NOTA: No caso do exemplo acima o codigo retorna true porque Code foi encontrado na string freeCodeCamp.


