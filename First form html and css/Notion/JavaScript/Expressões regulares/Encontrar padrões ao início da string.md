Desafios anteriores mostraram que expressões regulares podem ser usadas para capturar um número de resultados. Elas também podem ser usadas para procurar em posições específicas de strings.

Mais cedo você usou o circunflexo (`^`) em classes de caracteres para procurar caracteres que não devem ser capturados, como em `[^caracteresQueNãoQueremos]`. Quando usados fora de classes de caracteres, o circunflexo serve para buscar a partir do começo de strings.

```js
let firstString = "Ricky is first and can be found.";
let firstRegex = /^Ricky/;
firstRegex.test(firstString);
let notFirst = "You can't find Ricky now.";
firstRegex.test(notFirst);