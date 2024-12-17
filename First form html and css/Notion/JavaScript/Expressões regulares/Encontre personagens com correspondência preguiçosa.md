Em expressões regulares, uma correspondência gananciosa encontra a parte mais longa possível de uma string que se ajusta ao padrão regex e a retorna como uma correspondência. A alternativa é chamada de correspondência lenta, que encontra a menor parte possível da string que satisfaz o padrão regex.

Você pode aplicar a regex /t[a-z]*i/ à string "titanic". Este regex é basicamente um padrão que começa com t, termina com i e possui algumas letras entre eles.

Expressões regulares são gananciosas por padrão, então a correspondência retornaria ["titani"]. Ele encontra a maior substring possível para se ajustar ao padrão.

No entanto, você pode usar o ? caractere para alterá-lo para correspondência lenta. "titanic" corresponde ao regex ajustado de /t[a-z]*?i/ retorna ["ti"].

Nota: A análise de HTML com expressões regulares deve ser evitada, mas a correspondência de padrões de uma string HTML com expressões regulares é perfeitamente aceitável.

Fix the regex `/<.*>/` to return the HTML tag `<h1>` and not the text `"<h1>Winter is coming</h1>"`. Remember the wildcard `.` in a regular expression matches any character.

`let text = "<h1>Winter is coming</h1>";`

`let myRegex = /<h*?1>/; // Altere esta linha`

`let result = text.match(myRegex)`;`
