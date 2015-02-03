# JS Review
## Getting JS on the page
```
<script src=“main.js”></script>
```

```
<script>
  console.log(“Not a best practice”);

</script>
```

## Statements
A JS program is one or more JS statements
 
- One complete instruction to the computer
- End in semicolons

## values
## Primitives
- Boolean `true`, `false`
- String `”hello”`, `’goodbye’`
- Number `1`
## Objects
- Array
- Object
- Function
## Special case
```js
undefined // represents a value that is not defined
null // represents an object that is not defined
NaN // represents a Number that doesn’t make sense, e.g. 0 / 0
```
## variable
A container for a value

```
// Variable declaration
var a; // => undefined

// Variable assignment
a = ‘cool’;

// Combined
var b = ‘dumb’;
```

## expression
Code that evaluates to a value

```js
// a variable is an expression
a // => ‘cool’

// a variable declaration is also an expression
var c = ‘another thing’; // => undefined

// a variable assignment is an expression
c = ‘a third thing’; // => the rhs of the assignment, ‘a third thing’
```

**Mostly everything in JS is an expression / has a value**


## Functions
Objects that encapsulate zero or more JS statements.
- Zero or more arguments
- Zero or more explicit parameters
- Two implicit parameters (`this`, `arguments`)
- Zero or more side effects
- Exactly one return value, `undefined` by default

### Function Declaration
Is a JS statement

1. function keyword
2. function name
3. parameter list
4. function body

```js
function functionName(firstParameter) {
  // body
}
```
### Function Expression
Not a statement, it’s an expression, so it must be used as part of a statement.

```js
//      Expression V__________V
var functionName = function(){};

[(0 +1), 2, 3].forEach(function(i){
  console.log(i);
});

// Immediately Invoked Function Expression
(function(){

})();
```

## Scope
- Lexical (top to bottom)
- Variable declarations are hoisted to the top of their function, assignments are not
- Function declarations are hoisted in their entirety

## Arrays
### create
```js
var anArray = [1, 2, 3];
var secondArray = new Array(1, 2, 3);
```

### get a value
zero indexed
```js
anArray[1] // => 2
```

### set a value
```js
anArray[1] = 5;
anArray[100] = ‘cool’;
```

## Objects
```js
// properties
var cool = {
  name: “Jake”
}

// methods

var dog = {
  bark: function(){
    console.log(this); // => the dog
  }
}