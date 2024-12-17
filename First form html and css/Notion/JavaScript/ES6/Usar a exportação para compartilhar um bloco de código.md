Imagine um arquivo chamado `math_functions.js` que contém várias funções relacionadas a operações matemáticas. Uma delas é armazenada em uma variável, `add`, que recebe dois números e retorna a soma deles. Você quer usar essa função em diversos arquivos JavaScript diferentes. Para compartilhá-las com esses outros arquivos, você primeiro precisa exportá-las (`export`).

```js
export const add = (x, y) => {
  return x + y;
}
```

```
const add = (x, y) => {
  return x + y;
}

export { add };
```

```js
export { add, subtract };
```

Quando você exporta uma variável ou função, você pode importá-las em outro arquivo e usá-las sem ter de rescrever o código. Você pode exportar várias coisas ao repetir o primeiro exemplo para cada coisa que você queira exportar, ou ao colocar todas elas em uma instrução de export do segundo exemplo, da seguinte forma:

# Exportar apenas um valor com export default

Há outra sintaxe para `export` que você precisa saber, conhecida como exportação padrão. Você usará essa sintaxe quando apenas um valor estiver sendo exportado de um arquivo ou módulo. Essa sintaxe também é usada para exportar um valor substituto caso o valor original não possa ser exportado.

Abaixo estão exemplos utilizando a sintaxe `export default`:

```js
export default function add(x, y) {
  return x + y;
}

export default function(x, y) {
  return x + y;
}
```

NOTA: Em um arquivo pode haver apenas uma exportação padrão, e a diferença será na forma como importas elas, 

``import add from './path/to/module'; // Importa a função add como padrão
import { subtract } from './path/to/module'; // Importa a função subtract como nomeada

