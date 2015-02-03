## Prototypes and Constructors
### Constructors
A constructor is a function that is used to create objects. It's just a function
that is invoked by using the `new` keyword.

```js
// 1. Use strict mode
// 2. Use a capitalized name

// When invoked with `new`, `this` is the object being constructed
function Person(fullName){
  'use strict';

  this.firstName = fullName.split(' ')[0];
}

var person = new Person("Jake Smith");

```

The return value of a constructor is one of two things
1. If you *don't* return from a constructor, the value is `this`, which is set to an empty object
2. Whatever you return from the constructor, as long as it's an Object, otherwise it's `this`.

## Prototypes
Every function in JS has a prototype (sometimes it's undefined)
When you use a function as a constructor, that function's prototype becomes the
prototype of the constructed object

The properties (including methods) of an object's prototype are accessible on
that object

```js
function ATM(){
  this.balance = 0;
}

ATM.prototype.deposit = function(amount){
  this.balance = this.balance + amount;
  if(this.balance > this.maximumAmount){
    ATM.prototype.maximumAmount = this.balance;
  }
}

ATM.prototype.withdraw = function(amount){
  this.balance = this.balance - amount;
}

ATM.prototype.maximumAmount = 0;

var atm1 = new ATM();
var atm2 = new ATM();
atm1.deposit(10);
atm1.balance // => 10
atm2.balance // => 0
```

- a function + the `new` keyword == a constructor
- in a constructor, `this` is the object being constructed
- instanceof can be used to determine whether an object is an instance of a
  constructor
- Beware constructors in 'sloppy' mode, `this` == `window`, which can cause bad
  behavior when you forget the `new` keyword.
- Prototypes allow objects to inherit properties and functions from other
  objects in a hierarchy.
- Prototypes are wired up when you use the `new` keyword. The `.prototype` of
  the constructor function is connected to the instances of that constructor.
- `this` in a prototype's method is the instance that the method was called on.

    ```js

    function Dog(){}

    Dog.prototype.bark = function(){
      console.log(this.name + ' says woof');
    }

    var dog = new Dog();
    dog.name = "Fido";
    dog.bark(); // => Fido says woof
    ```
