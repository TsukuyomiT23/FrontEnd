The last challenge showed how to search for digits using the shortcut `\d` with a lowercase `d`. You can also search for non-digits using a similar shortcut that uses an uppercase `D` instead.

O atalho para procurar não dígitos é `\D`. Esse atalho é o mesmo que `[^0-9]`, que serve para procurar qualquer caractere que não seja um dígito de zero a nove.

---

Use o atalho `\D` para contar quantos não dígitos existem em títulos de filmes.

```let movieName = "2001: A Space Odyssey";

let noNumRegex = /\D/gi; // Altere esta linha

let result = movieName.match(noNumRegex).length;