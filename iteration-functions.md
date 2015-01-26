# Iteration Functions
## [forEach](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)

The reason to use forEach is have side effects for each item in an array.

### Examples
- Log each item
- Add something to an array or string for each item

```js
[1, 2, 3].forEach(function(num) {
  console.log(num);
});

// => 1
// => 2
// => 3
```

## map
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map
The reason to use map is to transform *each* item in the array and get a new
array.

Etiquette says that map should never have side effect, though this isn't
enforced in any way.

```js
[1, 2, 3].map(function(num) {
  return num * 2;
});

// => [2, 4, 6]
```

## filter
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter

The reason to use filter is to get a new array that only contains items that
match the criteria you're looking for.

The internal function must return `true` or `false`.

Etiquette says that filter should never have side effect, though this isn't
enforced in any way.

```js
[1, 2, 3].filter(function(num) {
  return num >= 3;
});
// => [3]
```

## reduce
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce

```js
[1, 2, 3].reduce(function(total, current) {
  return total + current;
});
// => 6
```

