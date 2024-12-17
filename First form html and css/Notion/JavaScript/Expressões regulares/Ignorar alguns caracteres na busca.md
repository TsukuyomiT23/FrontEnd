So far, you have created a set of characters that you want to match, but you could also create a set of characters that you do not want to match. These types of character sets are called negated character sets.

Para criar uma classe de caracteres negada, você só precisa colocar um acento circunflexo (`^`) depois do colchete de abertura e à esquerda dos caracteres que você quer evitar.

Por exemplo, `/[^aeiou]/gi` encontra todos os caracteres que não são vogais. Observe que caracteres como `.`, `!`, `[`, `@`, `/` e espaços em branco são capturados - a classe de vogais negada apenas exclui os caracteres que são vogais.

`let quoteSample = "3 blind mice.";`

`let myRegex = /[^aeiou0-9]/gi; // Altere esta linha`

`let result = quoteSample.match(myRegex); // Altere esta linha`