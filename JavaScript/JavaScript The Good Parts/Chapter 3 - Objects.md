## Types
In JavaScript there are 3 primitive types, numbers, strings, and Booleans. Then there are 2 special types, them being null and undefined. Everything else is an object. But what is an object?
## Objects
Objects are containers of properties. A property has a name and a value. Or key-value pairs. 
### Keys
The key can be any string, including an empty string `""`. It is important to note that the keys can also be reserved JavaScript keywords, you just must wrapped those in `""`, non JavaScript keywords do not have to me wrapped but can be. 
### Values
Values can be any JavaScript value except for `undefined`. This includes functions. And is the way you assign functions to objects. With an anonymous function as the value and the name you want to use to call the function as the key. Values can also contain other objects, allowing you to build tree like structures of objects
### Prototype
Every single object inherits a prototype object, this includes prototype itself
