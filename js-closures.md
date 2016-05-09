Closures are functions that refer to independent (free) variables. In other words, the function defined in the closure 'remembers' the environment in which it was created.

```js
function makeFunc() {
  var name = "Mozilla";
  function displayName() {
    alert(name);
  }
  return displayName;
}

var myFunc = makeFunc();
myFunc();
```
Example with IIFE and Module pattern

```
var FullName = (function(){

var name = "Peter"  // outer variable on which closure "closes over"

var closure = function (lastName) {
	return name+" "+lastName;

}

return closure;


})();

FullName("Smith") // "Peter Smith"
```

See [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)

> tags: closure, javascript, js