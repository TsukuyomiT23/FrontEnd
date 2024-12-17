Searching is useful. However, you can make searching even more powerful when it also changes (or replaces) the text you match.

Você pode buscar e substituir texto em uma string usando o método `.replace()`. O primeiro parâmetro do `.replace()` é o padrão regex que você quer procurar. O segundo parâmetro é a string que substituirá o resultado da busca ou uma função que fará algo com ele.

```js
let wrongText = "The sky is silver.";
let silverRegex = /silver/;
wrongText.replace(silverRegex, "blue");
```

A chamada a `replace` aqui retorna a string `The sky is blue.`.

Você também pode acessar grupos de captura na string de substituição usando o cifrão (`$`).

```js
"Code Camp".replace(/(\w+)\s(\w+)/, '$2 $1');
```

A chamada a `replace` aqui retorna a string `Camp Code`.

---

Escreva uma regex, `fixRegex`, que usa três grupos de captura para procurar cada palavra na string `one two three`. Depois atualize a variável `replaceText` para trocar de `one two three` para `three two one` e atribuir o resultado à variável `result`. Certifique-se de estar utilizando grupos de captura na string de substituição usando o cifrão (`$`).

```let str = "one two three";

let fixRegex = /^(\w+)\s(\w+)\s(\w+)/; // Altere esta linha

let replaceText = "$3 $2 $1"; // Altere esta linha

let result = str.replace(fixRegex, replaceText);