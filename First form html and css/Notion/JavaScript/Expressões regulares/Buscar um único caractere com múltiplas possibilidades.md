ou learned how to match literal patterns (`/literal/`) and wildcard character (`/./`). Those are the extremes of regular expressions, where one finds exact matches and the other matches everything. There are options that are a balance between the two extremes.

Você pode ter alguma flexibilidade ao procurar um padrão literal usando classes de caracteres. Classes de caracteres permitem a definição de grupos de caracteres que você quer capturar ao colocá-los entre colchetes: `[` e `]`.

Por exemplo, se você quiser encontrar `bag`, `big` e `bug` mas não `bog`. Você pode escrever a regex `/b[aiu]g/` para isso. `[aiu]` é a classe de caracteres que só capturará `a`, `i` ou `u`.

```js
let bigStr = "big";
let bagStr = "bag";
let bugStr = "bug";
let bogStr = "bog";
let bgRegex = /b[aiu]g/;
bigStr.match(bgRegex);
bagStr.match(bgRegex);
bugStr.match(bgRegex);
bogStr.match(bgRegex);
