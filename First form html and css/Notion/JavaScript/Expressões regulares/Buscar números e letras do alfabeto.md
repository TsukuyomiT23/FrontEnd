Using the hyphen (`-`) to match a range of characters is not limited to letters. It also works to match a range of numbers.

Por exemplo, `/[0-5]/` encontra qualquer número entre `0` e `5`, incluindo ambos `0` e `5`.

E também é possível combinar intervalos de letras e números em uma única classe de caracteres.

```js
let jennyStr = "Jenny8675309";
let myRegex = /[a-z0-9]/ig;
jennyStr.match(myRegex);
```
