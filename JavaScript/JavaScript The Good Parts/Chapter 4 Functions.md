## Function Objects
Just like everything else that isn't primitive or special, functions are objects. However they are different from typical objects since instead of being linked to `Object.prototype`functions are linked to `Function.prototype`. That being said, `Function.prototype` itself is linked to `Object.prototype`. Every function is also equipped with two additional hidden properties: context, and implements. However every function object also has a `prototype` property (different from both `Object.prototype` and `Function.prototype`) whose value is a `constructor` property, and that ones value is the function itself. Functions can be stored in variables, objects, arrays, passed as arguments to other functions, can be returned from functions, and themselves can have methods.
## Function Literals
You remember object literals? Its the same sort of thing here
```JS
var add = function (a, b){
	return a + b;
};
```