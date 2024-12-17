
Atualmente os usuários podem enviar o formulário sem verificar as entradas de rádio. Embora você tenha usado anteriormente o atributo obrigatório para indicar que uma entrada é obrigatória, ele não funcionará nesse caso porque adicionar o atributo obrigatório a ambas as entradas transmitirá informações erradas aos usuários.

Para resolver isso, você pode fornecer o contexto do que é necessário usando um elemento `legend` com o texto `Account type (required)` antes do elemento `label` dentro do segundo campo `fieldset`. Adicione então o atributo `checked` ao campo de entrada `Personal` input para garantir que o formulário foi enviado com o que era necessário neste.

<fieldset>

<legend>Account type (required)</legend>

<label ><input type="radio" name="account-type" checked/> Personal</label>

<label><input type="radio" name="account-type" /> Business</label>

</fieldset>