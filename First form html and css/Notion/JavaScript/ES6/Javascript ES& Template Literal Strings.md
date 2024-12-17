## Criando Strings usando Literais de Template

Um novo recurso do ES6 é o literal de template. Este é um tipo especial de string que facilita a criação de strings complexas.

Os literais de template permitem que você crie strings de várias linhas e utilize recursos de interpolação de strings.

Considere o código abaixo:
### Exemplo de código

```javascript
const person = {
  name: "Zodiac Hasbro",
  age: 56
};

const greeting = `Hello, my name is ${person.name}!
I am ${person.age} years old.`;

console.log(greeting);
```

O console exibirá as strings "Hello, my name is Zodiac Hasbro!" e "I am 56 years old.".

Muitas coisas aconteceram aqui. Primeiro, o exemplo usa crases (`` ` ``), e não aspas simples (`'`) ou duplas (`"`), para envolver a string. Em segundo lugar, observe que a string é de várias linhas, tanto no código quanto na saída. Isso elimina a necessidade de inserir `\n` dentro das strings. A sintaxe `${variável}` usada acima é um espaço reservado. Basicamente, você não precisará mais usar a concatenação com o operador `+`. Para adicionar variáveis a strings, você simplesmente coloca a variável dentro de um literal de template e a envolve com `${` e `}`. De forma semelhante, você pode incluir outras expressões no seu literal de string, por exemplo, `${a + b}`. Essa nova forma de criar strings oferece mais flexibilidade para criar strings robustas.

Use a sintaxe de literal de template com crases para criar um array de strings de elementos de lista (`li`). O texto de cada elemento da lista deve ser um dos elementos do array da propriedade `failure` do objeto `result` e ter um atributo de classe com o valor `text-warning`. A função `makeList` deve retornar o array de strings dos itens de lista.

Use um método de iteração (qualquer tipo de loop) para obter a saída desejada (mostrada abaixo).
### Exemplo de código

```javascript
[
  '<li class="text-warning">no-var</li>',
  '<li class="text-warning">var-on-top</li>',
  '<li class="text-warning">linebreak</li>'
]

const result = {

success: ["max-length", "no-amd", "prefer-arrow-functions"],

failure: ["no-var", "var-on-top", "linebreak"],

skipped: ["no-extra-semi", "no-dup-keys"]

};

function makeList(arr) {

// Altere apenas o código abaixo desta linha

const failureItems = [];

for (let i = 0; i < arr.length; i++) {

failureItems.push(`<li class="text-warning">${arr[i]}</li>`);

}

// Altere apenas o código acima desta linha

  

return failureItems;

}
```

NOTA MENTAL: O template literal de string apenas serve para concatenar strings a partir de variáveis ou elementos de objetos.