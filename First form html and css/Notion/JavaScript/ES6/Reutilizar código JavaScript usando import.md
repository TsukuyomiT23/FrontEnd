`import` allows you to choose which parts of a file or module to load. In the previous lesson, the examples exported `add` from the `math_functions.js` file. Here's how you can import it to use in another file:

```js
import { add } from './math_functions.js';
```

Aqui, `import` encontrará a função `add` no arquivo `math_functions.js`, importar apenas essa função e ignorar o resto. O `./` diz ao import para procurar pelo arquivo `math_functions.js` no mesmo diretório que o arquivo atual. O caminho relativo do arquivo (`./`) e a extensão do arquivo (`.js`) são necessários ao usar import dessa forma.

Você pode importar mais de um item do arquivo ao adicioná-los na instrução `import` dessa forma:

```js
import { add, subtract } from './math_functions.js';
```