## Equality (`==`)
- If two values have the same type, just compare them
- If two values have different types, try to coerce them into the same type and
  then compare them.

### Coersion
- When comparing a Number and String, coerce the String to a Number
- When comparing a Boolean and Anything, coerce the Boolean to a Number
- `null == undefined // => true`
- `NaN == NaN // => false`
- There can be multiple steps
  ```js
  /* 1 */ 1 == "" // coerce String -> Number
  /* 2 */ 1 == 0 // => false

  /* 1 */ "1" == true // coerce Boolean -> Number
  /* 2 */ "1" == 1 // coerce String -> Number
  /* 3 */ 1 == 1 // => true
  ```

## Strict equality

When using the strict equality operator (`===`), types are not coerced.

To put it another way, two expressions are strictly equal if they have the same
type and the same value.

## Object equality

Objects (including Arrays and Functions) are compared by reference. Two
references are equal only if they reference the same object.

```js
[1] === [1] // => false

var a = [1];
var b = a; // b is now a reference to the same object as a
a === b // => true
```

## Other coersion
- If you try to add anything to a String, the other operand is coerced to a
  String and the two Strings are concatenated
- To coerce an Object (including Arrays and Functions) to String, the
  `.toString` method is called on the Object
