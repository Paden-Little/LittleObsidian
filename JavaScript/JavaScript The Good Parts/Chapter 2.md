## Grammar
This section will largely show how JavaScript is structured as a language. It will pull diagrams from JavaScript: The Good Parts. 

This note will largely show how JavaScript is structured as a language. It will pull diagrams from JavaScript: The Good Parts. 
***
### Whitespace
Whitespace is any section of your code that doesn't have any characters present. It is sometimes necessary to separate certain tokens, and sometimes not necessary. That being said white space makes code a lot more readable
![[Pasted image 20230628184642.png]]
#### Comments
JS has 2 forms of comments.
	Block comments are formed by `/* */` where anything in the middle is a comment
	Line-ending comments are formed with `//` where the comment terminates at the end of the line
***
### Names
Naming things always start with a letter and then can optionally be followed with any number of letters numbers or underscores; Except for any language keywords of which there are many (I'm not listing them lol)
![[Pasted image 20230628190053.png]]
Names are used for statements, variables, parameters, property names, operators and labels.
***
### Numbers
JavaScript only has a single number type. a 64-bit floating point (same as java's double). There is also no separate Integer and floating point types, so `1` and `1.0` are the same value (thank god).
![[Pasted image 20230628191325.png]]
Negative numbers can be formed by the `-` prefix operator
#### `NaN`
`NaN` or not-a-number is returned whenever a numerical operation cannot return a numeric result. Typically means something has gone wrong. `NaN` is not equal to anything, including itself, so the only way to check for `NaN` is using the `isNaN(number)` function
***
### Strings
Strings are sequences of characters, the can be wrapped in single `''` or double quotes `""` and can contain zero or more characters
The `\` (backslash) is an escape character used to "escape" typical sequence. If you wanted to use single or double quotes in a string you would have to use the escape character
```Javascript
var myString = "She said \"Hi!\" to the boy."
```
JS does not have a character type, to do work on a character just use a string with one character in it.
![[Pasted image 20230628192632.png]]
All strings have a length property
```Javascript
lengthOfString = "seven".length //this is equal to 5
```
### Statements
By default, statements are executed top to bottom, with exceptions:
>the use of `if` and `switch` statements to choose what to execute.
>the use of `for`, `while`, and `do` statements we can loop and and repeat statements.
>the use of `break`, `return`, and `throw` statements which interrupt execution.
![[Pasted image 20230628195323.png]]
#### Var Statements
![[Pasted image 20230628194538.png]]
Whenever JS is ran, each time the browser sees a `<script>` tag the JavaScript file linked to it is immediately compiled and executed. 