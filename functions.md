# Functions
A function is a group of statements that can be called multiple times, and can be stored in a variable or passed around.

To put it another way: A function is an object that contains JavaScript code that is run when I call the function.

## Function declaration
A function declaration is a complete statement that can stand on its own. It creates a function with the name you specify.

```js
function coolFunction(thing) {
  alert(thing);
}
```

## Function expression
A function expression cannot stand on its own, but we can assign it to a variable or pass it to another function.

```js
var aFunction = function(thing) {
  alert(thing);
}

document.getElementById(id).addEventListener('click', function(){
  alert("Hay");
});
```
