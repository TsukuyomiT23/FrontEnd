Up until now, you've looked at regexes to do literal matches of strings. But sometimes, you might want to also match case differences.

Caixa (-alta ou -baixa) é a diferença entre letras maiúsculas e minúsculas. São exemplos de caixa alta: `A`, `B` e `C`. `a`, `b` e `c` são exemplos de caixa baixa.

Você pode encontrar ambas as caixas usando algo que chamamos de flag. Existem várias flags, mas agora nós queremos a flag que ignora a caixa - a flag `i`. Para usá-la é só colocar ao fim da regex. Por exemplo, escrever `/ignorecase/i` é uma forma. Essa regex pode encontrar as strings `ignorecase`, `igNoreCase` e `IgnoreCase` (e todas as outras combinações de maiúsculas e minúsculas).

#exemplo

l`et myString = "freeCodeCamp";`

`let fccRegex = /freeCodeCamp/i; // Altere esta linha`

`let result = fccRegex.test(myString);`
