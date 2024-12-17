You can specify the lower and upper number of patterns with quantity specifiers using curly brackets. Sometimes you only want a specific number of matches.

Para especificar este número, apenas escreva-o dentro das chaves.

Por exemplo, você pode escrever a regex `/ha{3}h/` para capturar a letra `a` `3` vezes na string `hah`.

```js
let A4 = "haaaah";
let A3 = "haaah";
let A100 = "h" + "a".repeat(100) + "h";
let multipleHA = /ha{3}h/;
multipleHA.test(A4);
multipleHA.test(A3);
multipleHA.test(A100);
```

As três chamadas a `test` acima retornam, na ordem, os valores: `false`, `true` e `false`.

---

```Modifique a regex `timRegex` para que capture quatro `m`s na string `Timber`.

let timStr = "Timmmmber";

let timRegex = /Tim{4}ber/; // Altere esta linha

let result = timRegex.test(timStr);