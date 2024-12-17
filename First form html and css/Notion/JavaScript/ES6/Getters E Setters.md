Set e get, são recursos para escrita e leitura de uma dado sem ter acesso direito ao mesmo dado, normalmente usados para aceder objetos...Ou seja serve para poder modificar e ler uma certa propriedade sem mostrar como funciona ou dar acesso direito ao usuário sobre a variável.

```js
class Book {
  constructor(author) {
    this._author = author;
  }
  // getter
  get writer() {
    return this._author;
  }
  // setter
  set writer(updatedAuthor) {
    this._author = updatedAuthor;
  }
}
const novel = new Book('anonymous');
console.log(novel.writer);
novel.writer = 'newAuthor';
console.log(novel.writer);
```

```class Thermostat {
  constructor(fahrenheit) {
    this._fahrenheit = fahrenheit; // Armazena a temperatura em Fahrenheit
  }

  // Getter para obter a temperatura em Celsius
  get celsius() {
    return (5 / 9) * (this._fahrenheit - 32);
  }

  // Setter para definir a temperatura em Celsius
  set celsius(celsius) {
    this._fahrenheit = celsius * 9.0 / 5 + 32;
  }
}

// Exemplo de uso da classe Thermostat
const therm = new Thermostat(68); // Inicializa com 68°F
console.log(therm.celsius); // Converte para Celsius e imprime

therm.celsius = 20; // Define a temperatura como 20°C
console.log(therm._fahrenheit); // Imprime a temperatura em Fahrenheit correspondente