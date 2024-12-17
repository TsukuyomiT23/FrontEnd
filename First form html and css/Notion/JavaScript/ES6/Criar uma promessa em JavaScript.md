Promessas são usadas para confirmar se uma ação foi cumprida ou não, desde ver se uma requisição no servidor foi aceita ou não, se o usuário preencheu um formulário ou não esperando a resposta dele(normalmente aquela pergunta depois de preencher que vem enviar ou cancelar), para outras questões de código também por exemplo pra saber quanto tempo levou uma operação e etc.

Uma promessa em JavaScript é exatamente o que parece - você faz a promessa de que vai fazer uma tarefa, geralmente de forma assíncrona. Quando a tarefa é finalizada, ou você cumpriu a promessa ou falhou ao tentar. Por ser uma função construtora, você precisa utilizar a palavra-chave `new` para criar uma `Promise`. Ela recebe uma função, como seu argumento, com dois parâmetros - `resolve` e `reject`. Esses métodos são usados para determinar o resultado da promessa. A sintaxe se assemelha a:

```js
const myPromise = new Promise((resolve, reject) => {

});
```

# Concluir uma promessa com resolve e reject

Uma promessa tem três estados: pendente, cumprida e rejeitada. A promessa que você criou no último desafio ficará para sempre presa no estado pendente porque você não adicionou uma forma de cumprir a promessa. Os parâmetros de resolução e rejeição fornecidos ao argumento da promessa são usados ​​para fazer isso. resolver é usado quando você deseja que sua promessa seja bem-sucedida e rejeitar é usado quando você deseja que ela falhe. Esses são métodos que aceitam um argumento, conforme visto abaixo.

```js
const myPromise = new Promise((resolve, reject) => {
  if(condition here) {
    resolve("Promise was fulfilled");
  } else {
    reject("Promise was rejected");
  }
});
```

# Manipular uma promessa cumprida usando o then

Promessas são úteis quando você tem um processo que leva uma quantidade de tempo desconhecido para ser finalizado (ou seja, algo assíncrono). Muitas vezes, uma requisição a um servidor. Fazer uma requisição a um servidor leva tempo, e após a requisição ser finalizada, você geralmente quer fazer algo com a resposta retornada. Isso pode ser feito usando o método `then`.

```js
Promise.prototype.then(onFulfilled, onRejected)
```

O método `then` agenda as funções de callback para a eventual conclusão de uma promise – seja satisfazendo a promise ou a rejeitando. Um dos manipuladores, `onFulfilled` e `onRejected`, será executado para lidar com o cumprimento da promise ou com sua rejeição atual. Quando a promise é cumprida com `resolve`, o manipulador `onFulfilled` é chamado.

```js
myPromise.then(result => {

});
```

O parâmetro `result` vem do argumento dado ao método `resolve`.

# Manipular uma promessa rejeitada usando o catch

catch é o método usado quando sua promessa foi rejeitada. Ele é executado imediatamente após o método de rejeição de uma promessa ser chamado. Aqui está a sintaxe:

```js
myPromise.catch(error => {

});
```

