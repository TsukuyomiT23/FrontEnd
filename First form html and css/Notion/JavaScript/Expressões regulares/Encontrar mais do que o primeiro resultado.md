Para buscar ou extrair um padrão além do primeiro resultado, você pode usar a flag de busca global `g`.

```js
let repeatRegex = /Repeat/g;
testStr.match(repeatRegex);