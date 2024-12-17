The last challenge used the plus `+` sign to look for characters that occur one or more times. There's also an option that matches characters that occur zero or more times.

O caractere usado para isso é o asterisco: `*`.

Nota: Ele retorna mesmo se não encontra o caractere pedido, retorna uma string vazia;

```js
let soccerWord = "gooooooooal!";
let gPhrase = "gut feeling";
let oPhrase = "over the moon";
let goRegex = /go*/;
soccerWord.match(goRegex);
gPhrase.match(goRegex);
oPhrase.match(goRegex);
```

As três chamadas a `match` retornam, na ordem, os valores: `["goooooooo"]`, `["g"]` e `null`
