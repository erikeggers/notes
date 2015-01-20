# Falsy
- `""`
- `0`
- `false`
- `undefined`
- `null`
- `NaN`

# Truthy
Everything else

```js
var name = "";
if(name){
  // this will not happen
  alert(name);
}
```
