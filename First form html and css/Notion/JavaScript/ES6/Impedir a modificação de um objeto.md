As seen in the previous challenge, `const` declaration alone doesn't really protect your data from mutation. To ensure your data doesn't change, JavaScript provides a function `Object.freeze` to prevent data mutation.

Qualquer tentativa de alterar o objeto será rejeitada, com um erro sendo lançado se o script estiver executando em modo estrito.

``````js
let obj = {
  name:"FreeCodeCamp",
  review:"Awesome"
};
Object.freeze(obj);
obj.review = "bad";
obj.newProp = "Test";
console.log(obj); 
´´´

As atribuições `obj.review` e `obj.newProp` vão resultar em erros, pois nosso editor executa em modo estrito por padrão. O console vai exibir o valor `{ name: "FreeCodeCamp", review: "Awesome" }`.

---

Nesse desafio, você usará o método `Object.freeze` para prevenir a mudança de constantes matemáticas. Você precisa congelar o objeto `MATH_CONSTANTS` para que ninguém possa alterar o valor de `PI`, adicionar ou deletar propriedades.


NOTA: Ao declarar um objeto com a palavra-chave const nós apenas impedidos que declare outra variavel com o mesmo nome, mas para impedir alteração de mudança de dados precisamos usar a função Object.frezee.