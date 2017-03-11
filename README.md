# node-js-snippets

EventEmitter example:
```javascript
const EventEmitter = require('events').EventEmitter;

class Person extends EventEmitter {
  constructor(name, walkingTime) {
    super();
    this.name = name;
    this.walkingTime = walkingTime;
    this.on('stopWalking', () => {
      setTimeout(() => {
        console.log(`${this.name} закончил гулять спустя ${Math.ceil(this.walkingTime / 1000)} cекунды.`)
      }, this.walkingTime);
    })
    this.on('walking', () => {
      console.log(`${this.name} начал прогулку...`);
      this.emit('stopWalking');
    })
  }
  walk() {
    this.emit('walking');
  }
}

const person1 = new Person('Evgeny', 2000);
const person2 = new Person('Alex', 5000);

person1.walk();
person2.walk();

// => Evgeny начал прогулку...
// => Alex начал прогулку...
// => Evgeny закончил гулять спустя 2 cекунды.
// => Alex закончил гулять спустя 5 cекунды.
```
