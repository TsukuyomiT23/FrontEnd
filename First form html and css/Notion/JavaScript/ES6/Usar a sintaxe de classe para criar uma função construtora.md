ES6 provides a new syntax to create objects, using the class keyword.

No ES5, um objeto pode ser criado definindo uma função `constructor` e usando a palavra-chave `new` para instanciar o objeto.

No ES6, uma declaração de `class` tem um método `constructor`, que é invocado com a palavra-chave `new`. Se o método `constructor` não for explicitamente definido, ele será definido implicitamente sem argumentos.

Exemplo de código

```js
// Explicit constructor
class SpaceShuttle {
  constructor(targetPlanet) {
    this.targetPlanet = targetPlanet;
  }
  takeOff() {
    console.log("To " + this.targetPlanet + "!");
  }
}

// Implicit constructor 
class Rocket {
  launch() {
    console.log("To the moon!");
  }
}

const zeus = new SpaceShuttle('Jupiter');
// prints To Jupiter! in console
zeus.takeOff();

const atlas = new Rocket();
// prints To the moon! in console
atlas.launch();
```

Nota: As classes são formas de criar funções com objetos dentro dela, onde temos que usar um construtor que é uma função para criar o objeto, essa palavra chave construtor pode estar explicito ou não;