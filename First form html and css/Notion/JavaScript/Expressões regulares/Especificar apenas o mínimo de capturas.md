You can specify the lower and upper number of patterns with quantity specifiers using curly brackets. Sometimes you only want to specify the lower number of patterns with no upper limit.

Para fazer isso, apenas escreva o número seguido de uma vírgula dentro das chaves.

Por exemplo, para capturar pelo menos `3` vezes a letra `a` na string `hah` você pode escrever a regex `/ha{3,}h/`.

```js
let A4 = "haaaah";
let A2 = "haah";
let A100 = "h" + "a".repeat(100) + "h";
let multipleA = /ha{3,}h/;
multipleA.test(A4);
multipleA.test(A2);
multipleA.test(A100);
```

As três chamadas a `test` acima retornam, na ordem, os valores: `true`, `false` e `true`.

---

Modifique a regex `haRegex` para que capture quatro ou mais `z`s na string `Hazzah`.

```let haStr = "Hazzzzah";

let haRegex = /Haz{4,}ah/; // Altere esta linha

let result = haRegex.test(haStr);