# Inheritance
To set up hierarchical prototype chains, you must:
1. Connect the prototypes of the various constructors together.
2. Call the "parent" constructor function from the "child" constructor function.

```js
function Animal(options) {
  this.color = options.color;
}

Animal.prototype.walk = function(){
  console.log('walking...');
}

function Dog(options) {
  Animal.call(this, options);

  this.breed = options.breed;
}

Dog.prototype = Object.create(Animal.prototype);

Dog.prototype.bark = function(){
  console.log('woof');
}

var finn = new Dog({
  color: 'yellow',
  breed: 'Golden Retriever'
});
```
