
ES6 adds some nice support for easily defining object literals.

Considere o seguinte código:

Exemplo de código

``````js
const getMousePosition = (x, y) => ({
  x: x,
  y: y
});
```

`getMousePosition` é uma função simples que retorna um objeto contendo duas propriedades. ES6 fornece o açúcar sintático para eliminar a redundância de ter de escrever `x: x`. Você pode simplesmente escrever `x` uma vez, e será convertido para `x: x` (ou algo equivalente). Aqui está a mesma função que acima rescrita para usar a nova sintaxe:

Exemplo de código

```js
const getMousePosition = (x, y) => ({ x, y });
```

NOTA: Esse tema aborda a possibilidade de evitar redundancia de escrever os nome das propriedades de um objecto e o seu conteúdo quando os mesmos são iguais
