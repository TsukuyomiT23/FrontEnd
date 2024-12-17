In the last challenge, you searched for the word `Hello` using the regular expression `/Hello/`. That regex searched for a literal match of the string `Hello`. Here's another example searching for a literal match of the string `Kevin`:

```js
let testStr = "Hello, my name is Kevin.";
let testRegex = /Kevin/;
testRegex.test(testStr);
```

Essa chamada a `test` retornará `true`.

Qualquer outra forma de escrever `Kevin` não funcionará. Por exemplo, a regex `/Kevin/` não encontrará nem `kevin` e nem `KEVIN`.

```js
let wrongRegex = /kevin/;
wrongRegex.test(testStr);
```

Nota: Dessa forma retornará false.