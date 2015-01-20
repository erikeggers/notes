# [Arithmetic
Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators)

```js
4 + 3 // => 7
4 - 3 // => 1
4 * 3 // => 12
12 / 5 // => 2.4
12 % 5 // => 2
```

# [Comparison
Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators)
## Loose (they coerce the type)

```js
"cool" == "cool" // => true
"cool" != "dumb" // => true
1 == "1" // => true (it coerces the number into a string)
0 != false // => false (it coerces the number into a boolean)
12 > 5 // => true
12 >= 12 // => true
12 < 36 // => true
12 <= 12 // => true
```

## Strict (do not coerce the type)

```js
"cool" === "cool" // => true
"1" === 1 // => false
0 !== false // => true
```

# [Logical
Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_Operators)

```js
!true // => false
!(10 > 5) // => false

true && true // => true
true && false // => false
(10 > 5) && (10 < 100) // => true
(10 > 5) && (10 < 10) // => false

true || true // => true
true || false // => true
false || false // => false
(10 > 5) || (10 < 100) // => true
(10 > 5) || (10 < 10) // => true
```

# [Assignment
Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Assignment_Operators)
There are many available, but a couple of examples:

```js
var x;

x = 2;
x // => 2

x += 2;
x // => 4
```
