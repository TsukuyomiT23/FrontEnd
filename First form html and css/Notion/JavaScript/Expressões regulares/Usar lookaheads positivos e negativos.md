Lookaheads are patterns that tell JavaScript to look-ahead in your string to check for patterns further along. This can be useful when you want to search for multiple patterns over the same string.

Existem dois tipos de lookahead: o lookahead positivo e o lookahead negativo.

Lookaheads positivos garantem que o padrão especificado se encontra à frente, mas não o capturam. Usa-se `(?=...)`, onde `...` é o padrão a ser procurado, para escrever lookaheads positivos.

Lookaheads negativos, por outro lado, garantem que o padrão especificado não se encontra à sua frente na string. Para usar lookaheads negativos, escrevemos `(?!...)` onde `...` é o padrão que você quer ter certeza que não está lá. O restante do padrão é validado se o padrão do lookahead negativo estiver ausente.

É fácil se confundir com lookaheads, mas uns exemplos podem ajudar.

```js
let quit = "qu";
let noquit = "qt";
let quRegex= /q(?=u)/;
let qRegex = /q(?!u)/;
quit.match(quRegex);
noquit.match(qRegex);
```

As duas chamadas a `match` retornam `["q"]`.

Validar dois padrões diferentes em uma string é considerado um uso mais prático de lookaheads. Neste não tão aprimorado validador de senhas, os lookaheads procuram por 3 a 6 caracteres e pelo menos um número, respectivamente, na string:

```js
let password = "abc123";
let checkPass = /(?=\w{3,6})(?=\D*\d)/;
checkPass.test(password);
```

---

Use os lookaheads na `pwRegex` para que correspondam a senhas de mais de 5 caracteres e que tenham dois algarismos consecutivos.

Claro! Vamos explicar melhor sobre lookaheads em JavaScript.

### O que são Lookaheads?

Lookaheads são padrões usados em expressões regulares que permitem que o JavaScript "olhe para frente" em uma string para verificar a presença de padrões específicos. Isso é útil quando você deseja procurar múltiplos padrões dentro da mesma string.

### Tipos de Lookaheads

Existem dois tipos principais de lookaheads:

1. **Lookahead Positivo**: 
   - Garante que um padrão específico esteja presente à frente, mas não o captura. 
   - A sintaxe é `(?=...)`, onde `...` representa o padrão que você está procurando.
   - **Exemplo**: Se você tem o padrão `q(?=u)`, isso significa "encontre `q` que é seguido por `u`".

2. **Lookahead Negativo**:
   - Garante que um padrão específico não esteja presente à frente na string.
   - A sintaxe é `(?!...)`, onde `...` é o padrão que você quer garantir que não esteja presente.
   - **Exemplo**: Com o padrão `q(?!u)`, significa "encontre `q` que não é seguido por `u`".

### Exemplos Práticos

Para ilustrar, considere os seguintes exemplos:

```javascript
let quit = "qu";
let noquit = "qt";
let quRegex = /q(?=u)/; // Lookahead positivo
let qRegex = /q(?!u)/;  // Lookahead negativo

console.log(quit.match(quRegex));  // Retorna ["q"]
console.log(noquit.match(qRegex));  // Retorna ["q"]
```

Ambas as chamadas a `match` retornam `["q"]`, demonstrando como os lookaheads funcionam.

### Uso Prático

Lookaheads são especialmente úteis para validar padrões em strings. Por exemplo, se quisermos validar uma senha que deve ter entre 3 a 6 caracteres e pelo menos um número, podemos usar:

```javascript
let password = "abc123";
let checkPass = /(?=\w{3,6})(?=\D*\d)/; // Lookaheads para validar a senha

console.log(checkPass.test(password)); // Retorna true
```

### Exercício

Agora, você pode usar lookaheads na expressão `pwRegex` para criar uma validação que corresponda a senhas com mais de 5 caracteres e que tenham dois dígitos consecutivos. 

Se precisar de ajuda em como implementar isso, sinta-se à vontade para perguntar!

A expressão `(?=\D*\d)` é um exemplo de lookahead positivo em uma expressão regular e pode ser decomposta da seguinte forma:

1. **`(?=...)`**: Esta parte indica que estamos usando um lookahead positivo. Isso significa que o padrão que segue deve estar presente à frente na string, mas não será capturado.

2. **`\D*`**: 
   - `\D` é um metacaractere que representa qualquer caractere que **não** seja um dígito (ou seja, não é de 0 a 9).
   - O asterisco `*` significa "zero ou mais" ocorrências do padrão anterior. Portanto, `\D*` corresponde a qualquer quantidade de caracteres não numéricos, incluindo a possibilidade de não haver nenhum.

3. **`\d`**: 
   - `\d` é um metacaractere que representa qualquer dígito (ou seja, de 0 a 9).

### Juntando Tudo

Então, `(?=\D*\d)` significa que, para que uma correspondência ocorra, deve haver zero ou mais caracteres não numéricos seguidos por pelo menos um dígito adiante na string. Isso é útil para garantir que, em uma string, exista pelo menos um número, independentemente de quantos caracteres não numéricos estão antes dele.

### Exemplo

Se tivermos a string `"abc123"`, o lookahead `(?=\D*\d)` verificará:

- `abc` são caracteres não numéricos (correspondendo a `\D*`).
- `1` é um dígito (correspondendo a `\d`).

Portanto, o lookahead será verdadeiro, pois a condição é satisfeita.

```let sampleWord = "astronaut";

let pwRegex = /^(?=\w{6})(?=\w*\d{2})/; // Altere esta linha

let result = pwRegex.test(sampleWord);