Usando classes de caracteres, você foi capaz de pesquisar todas as letras do alfabeto com [a-z]. Esse tipo de classe de caracteres é comum o suficiente para que exista um atalho para ela, embora também inclua alguns caracteres extras.

A classe de caracteres mais próxima em JavaScript que corresponde ao alfabeto é \w. Este atalho é igual a [A-Za-z0-9_]. Esta classe de caracteres corresponde a letras maiúsculas e minúsculas, além de números. Observe que esta classe de caracteres também inclui o caractere sublinhado (_).

```let quoteSample = "The five boxing wizards jump quickly.";

let alphabetRegexV2 = /\w+/gi; // Altere esta linha

let result = quoteSample.match(alphabetRegexV2).length;
