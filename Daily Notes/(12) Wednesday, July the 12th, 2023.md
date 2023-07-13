[[(11) Tuesday, July the 11th, 2023]] #InteractiveWebDev #OpenSourcePlatformsDev #Javascript #Prototype #NodeJS #Regex 
## Interactive Web Dev
### Debugging in Node.js
Shull hates `console.log()`. There is not a lot of information for testing and viewing behavior with `console.log()` For example, if you log an object, it will list key value pairs properly, but any functions within with not work. However strings, and other special built in objects with have special prints. Node has proper debugging functionality.
#### Prototype 
Prototype is assigned to every object (remember functions are objects but primitives are not (this includes strings)). Prototype is an object itself so each prototype will have a prototype until it returns null. And prototype has those blanket statements like `constructor()` or `toString()` that all objects just have. Whenever you would call `toString()` for example, the engine looks for `toString()` in the base object, and if it can't find it then it goes to the Prototype and executes its implementation of `toString()`. 

## Open source platforms development
### Regex
Regex is syntactic rules not a language. However most languages will have an implementation of regex since its so well known and so powerful
"My mother told me you are a liar"
- `[]` - Matches any characters within the brackets
	- `[tom]` will match all the `m`'s  `t`'s and `o`'s
	- `[a-z]` will find all lowercase letters - equivalent to `\d`
	- `[a-z]{3}` will find any letters that occur 3 times in a row
- `?` - Between zero and once
- `*` - Zero or more
- `+` - One or more
- `\w` - A single character alphanumeric, upper and lower. Excludes punctuation and anything else
- `^` - Search for start of line
	- `^My` will match the My in our test string
- `$` - Search end of line
	- `liar$` will match liar
- `.+` will return everything
- `.*` - Will get everything or nothing at all
- #### Groups
	- Groups will find anything between 2 strings
	- `mother(.+)you` will match " told me " whitespace included
