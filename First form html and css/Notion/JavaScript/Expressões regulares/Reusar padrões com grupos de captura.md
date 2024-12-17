Say you want to match a word that occurs multiple times like below.

```js
let repeatStr = "row row row your boat";
```

Você poderia usar `/row row row/`, mas e se você não souber a palavra específica repetida? Grupos de captura podem ser usados para localizar substrings repetidas.

Os grupos de captura são criados envolvendo o padrão de regex a ser capturado entre parênteses. Neste caso, o objetivo é capturar uma palavra composta de caracteres alfanuméricos para que o grupo de captura seja `\w+` entre parênteses: `/(\w+)/`.

A substring correspondente ao grupo é salva em uma "variável" temporária que pode ser acessada dentro da mesma expressão regular usando uma barra invertida e o número do grupo de captura (ex.: `\1`). Os grupos de captura são automaticamente numerados pela posição de abertura de seus parênteses (esquerda para direita), começando em 1.

O exemplo abaixo captura qualquer palavra que se repita três vezes, separada por espaços:

```js
let repeatRegex = /(\w+) \1 \1/;
repeatRegex.test(repeatStr); // Returns true
repeatStr.match(repeatRegex); // Returns ["row row row", "row"]
```

Usar o método `.match()` em uma string retornará um array com a substring correspondente, juntamente com seus grupos capturados.

---

Use grupos de captura na regex `reRegex` para capturar em uma string um número que aparece exatamente três vezes, separados por espaços.

```let repeatNum = "42 42 42";

let reRegex = /^(\d+) \1 \1(?!.)/; // Altere esta linha

let result = reRegex.test(repeatNum);

Vamos analisar a expressão regular `/^(\d+) \1 \1(?!.)/` passo a passo:

### Componentes da Regex

1. **`^`**:
   - Indica o início da string. A correspondência deve começar aqui.

2. **`(\d+)`**:
   - Este é um grupo de captura que corresponde a um ou mais dígitos (`\d` representa qualquer dígito de 0 a 9).
   - O `+` indica que deve haver pelo menos um dígito.

3. **` \1`**:
   - O espaço em branco (` `) indica que deve haver um espaço após o primeiro grupo de dígitos.
   - `\1` refere-se ao primeiro grupo de captura, ou seja, os dígitos que foram encontrados anteriormente. Isso significa que a mesma sequência de dígitos deve aparecer novamente.

4. **` \1`**:
   - Outro espaço em branco seguido de `\1`, que novamente refere-se ao primeiro grupo de captura. Portanto, a sequência de dígitos deve aparecer uma terceira vez.

5. **`(?!.)`**:
   - Este é um lookahead negativo. Ele garante que **não** haja mais nenhum caractere após os três grupos de dígitos.
   - O `.` representa qualquer caractere, e o `?!` assegura que não existe nada nesse espaço.

### Resumo

A expressão regular completa `/^(\d+) \1 \1(?!.)/` busca por uma string que:

- Começa com uma sequência de um ou mais dígitos.
- Segue com um espaço.
- Repete a mesma sequência de dígitos mais duas vezes, cada uma seguida por um espaço.
- Não contém nenhum outro caractere após essa sequência.

### Exemplo de Correspondência

- **`"123 123 123"`**: Corresponde (todas as partes se encaixam).
- **`"456 456 456 "`**: Não corresponde (tem um espaço extra no final).
- **`"789 789"`**: Não corresponde (falta um terceiro grupo).

Essa regex é útil para verificar padrões repetitivos de números em uma string. Se precisar de mais detalhes ou exemplos, é só avisar!