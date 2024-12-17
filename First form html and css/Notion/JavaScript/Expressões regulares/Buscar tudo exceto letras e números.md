You've learned that you can use a shortcut to match alphanumerics `[A-Za-z0-9_]` using `\w`. A natural pattern you might want to search for is the opposite of alphanumerics.

Você pode capturar não alfanuméricos usando `\W` ao invés de `\w`. Observe que o atalho usa uma maiúscula. Este atalho é o mesmo que escrever `[^A-Za-z0-9_]`.

```let quoteSample = "The five boxing wizards jump quickly.";

let nonAlphabetRegex = /\W/gi; // Altere esta linha

let result = quoteSample.match(nonAlphabetRegex).length;