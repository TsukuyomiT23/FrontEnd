You learned about searching for whitespace using `\s`, with a lowercase `s`. You can also search for everything except whitespace.

Busque não espaços em branco usando `\S` com um `s` maiúsculo. Este atalho não captura espaços em branco, retorno de carro, tabulações, feeds de formulário ou quebras de linha. O atalho é equivalente à classe de caracteres `[^ \r\t\f\n\v]`.

```js
let whiteSpace = "Whitespace. Whitespace everywhere!"
let nonSpaceRegex = /\S/g;
whiteSpace.match(nonSpaceRegex).length;
```

O valor retornado pelo método `.length` aqui é `32`.

---

Modifique a regex `countNonWhiteSpace` para que encontre tudo exceto espaços em branco em uma string.

