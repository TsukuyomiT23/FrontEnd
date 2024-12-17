When defining functions within objects in ES5, we have to use the keyword `function` as follows:

Exemplo de código

``````js
const person = {
  name: "Taylor",
  sayHello: function() {
    return `Hello! My name is ${this.name}.`;
  }
};
```

aplicando alteração apenas nos permite remover a palavra-chave function e os dois pontos ficando desse jeito;

```js
const person = {
  name: "Taylor",
  sayHello() {
    return `Hello! My name is ${this.name}.`;
  }
};
```