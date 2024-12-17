Sometimes, you need to match a character (or group of characters) that appears one or more times in a row. This means it occurs at least once, and may be repeated.

Você pode usar o caractere `+` para verificar se é o caso. Lembre-se que o caractere ou padrão precisa repetir-se consecutivamente. Ou seja, um atrás do outro.

Por exemplo, `/a+/g` encontra um resultado na string `abc` e retorna `["a"]`. Mas o `+` também faz com que encontre um único resultado em `aabc` e retorne `["aa"]`.

Se a string fosse `abab`, a operação retornaria `["a", "a"]` porque entre os dois `a` há um `b`. Por fim, se não houvesse nenhum `a` na string, como em `bcd`, nada seria encontrado.

Nota: Ele apenas retorna se o caractere aparece uma ou mais vezes...ou seja ele só retorna se encontrar o caracter pedido

Para a string `"goib"` e a expressão regular `ga+`, vamos analisar o que acontece:

```javascript
let testString = "goib";
let gaRegex = /ga+/;
let result = testString.match(gaRegex);
console.log(result);
```

### Resultado:
A chamada `match(gaRegex)` retornará `null`. 

### Explicação:
- A expressão regular `ga+` procura pela letra "g" seguida por uma ou mais letras "a" consecutivas.
- Na string `"goib"`, não há nenhuma sequência que comece com "g" e seja seguida por pelo menos uma "a". Portanto, não há correspondência, resultando em `null`.


