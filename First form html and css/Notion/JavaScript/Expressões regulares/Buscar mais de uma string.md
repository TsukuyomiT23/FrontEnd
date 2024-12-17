Ao usar regexes como `/coding/`, você pode procurar pelo padrão `coding` em strings.

Isso funciona com strings únicas, mas é limitado a apenas um padrão. Você pode procurar por múltiplos padrões usando o operador de `alternation`, ou `OR`: `|`.

Este operador funciona para buscar padrões à esquerda e à direita dele. Por exemplo, se você quiser encontrar as strings `yes` ou `no`, a regex que você quer é `/yes|no/`.

Você pode também procurar por mais de dois padrões com este operador. É possível fazer isso ao adicionar mais instâncias do operador seguido do padrão desejado: `/yes|no|maybe/`.