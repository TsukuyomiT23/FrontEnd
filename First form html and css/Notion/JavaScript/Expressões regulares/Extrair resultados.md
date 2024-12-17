Até agora, você só tem verificado se existe ou não um padrão dentro de uma string. Você também pode extrair os resultados encontrados por meio do método `.match()`.

Para usar o método `.match()`, aplique o método em uma string e passe a regex dentro dos parênteses.

Exemplo:

```js
"Hello, World!".match(/Hello/);
let ourStr = "Regular expressions";
let ourRegex = /expressions/;
ourStr.match(ourRegex);
```

Aqui, o primeiro `match` retorna `["Hello"]` e, o segundo, `["expressions"]`.

Note que o método `.match` se usa de forma "contrária" ao método `.test` que você usou até então:

```'string'.match(/regex/); //antes do metódo leva a string e como argumento a palavra a ser procura
/regex/.test('string'); //Aqui é o contrário...
