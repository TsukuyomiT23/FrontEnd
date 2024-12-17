Tal como quase todo formulário, em questões de preenchimento são establecidas algumas regras como por exemplo o tipo de caracteres devem ser colocados, como por exemplo se são letras maiúsculas ou minúsculas, e o intervalo delas, ou mesmo digito e o seu intervalo.

Podemos usar o atributo pattern para isso e também é possivel definir o valor mínimo de caracteres aceites.

Adicione um atributo `pattern` ao elemento `input` de senha para exigir que a entrada corresponda aos valores: `[a-z0-5]{8,}`

O comando acima é uma expressão regular que corresponde a oito ou mais letras minúsculas ou os dígitos de `0` a `5`. Agora, remova o atributo `minlength` e experimente-o.

<label for="new-password">Create a New Password: <input id="new-password" type="password" pattern="[a-z0-5]{8,}" required /></label>