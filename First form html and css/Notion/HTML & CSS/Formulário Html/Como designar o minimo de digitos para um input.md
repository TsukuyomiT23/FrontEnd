No caso de email tem a questão de que o email deve ser válido esperando-se um email que contenha um @ e um . acompanhado da sua extensão.

No caso de palavra passe para exigir um número de caracter mínimo usamos Adicione uma validação personalizada ao elemento `input` de senha, adicionando um atributo `minlength` com um valor de `8`. Isso evita que entradas com menos de 8 caracteres sejam enviadas.

<label for="new-password">Create a New Password: <input id="new-password" type="password" minlenght="8" required /></label>