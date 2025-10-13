# Coding Tip #36: Understand Prototype Inheritance in JavaScript

JavaScript is based on prototype-based inheritance, meaning that objects can inherit properties and methods from other objects. Understanding this concept is key to mastering JavaScript and building efficient object-oriented code.

**Tip**: Learn how to use prototypes and inheritance to share functionality between objects without duplicating code.

Example of prototype inheritance:
```js
function Animal(name) {
  this.name = name;
}

Animal.prototype.sayHello = function() {
  console.log('Hello, ' + this.name);
};

const dog = new Animal('Rex');
dog.sayHello(); // "Hello, Rex"

// Dog-specific behavior
function Dog(name, breed) {
  Animal.call(this, name);  // Inherit from Animal
  this.breed = breed;
}

Dog.prototype = Object.create(Animal.prototype);  // Set prototype chain
Dog.prototype.constructor = Dog;

const myDog = new Dog('Max', 'Bulldog');
myDog.sayHello(); // "Hello, Max"
```

In the example above, the Dog object inherits the `sayHello` method from the Animal object using prototype chaining. This allows Dog to have its own properties but still access methods defined in Animal.

You can extend this concept with more advanced inheritance patterns, such as mixins, to create more flexible and reusable code.


---

Thanks!


🚀Keep Coding, Keep Growing!!
