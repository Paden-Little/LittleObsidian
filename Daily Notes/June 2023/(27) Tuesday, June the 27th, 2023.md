[[(26) Monday, June the 26th, 2023]] #InteractiveWebDev #DatabasesII 
## Interactive Web Dev
#### What is Javascript?
- Javascript is a scripting language primarily developed for interactive websites
- A scripting language is **not compiled** and instead interpreted by an engine.
	- If run from a website it’s interpreted in the browser 
	- Node.js for example is a removed from browser interpreter for javascript
#### Console.log
```Javascript
console.log(“Print something to the log”)
```
- `console.log()`  is a method that takes any type of object and any number of objects and prints whatever data it can find to the console
#### Functions
```Javascript
function doSomething(firstNumber, secondNumber){
	return firstNumber + secondNumber
}
```
- The function signature is like the “name” of the function, the actually name, here “doSomething” then the parameters, here “firstNumber, secondNumber”.
- Whenever this function is called it takes what you give it, does stuff then either ends or returns
- For this example it takes the two numbers and adds them together and returns them
- **NOTE**: We have no way to guarantee what we get from the method caller is a number, it could be any object
- ##### Function = defintion
	- Functions can also be defined as a variable 
```JavaScript
var doSomeMaths = function(firstNumber, secondNumber){
	return firstNumber + secondNumber
}
```
- Doing a function definition this way makes it so that we have more control over the function
	- This allows us to define a function that is only executable in a certain scope, meaning garbage collection removes the variable reference and all the function code whenever we leave the scope
	- It also allows us to make a function call non-global. If we define a function normally anywhere in the script we can access it anywhere else in the script, with this notation we can only access that function after the variable for it is declared. 
		- This means we can also change the function as our script is executed. If after a condition is met or after a certain point in the code we could reassign the variable holding the original function, to an entirely new function that changes anything about the function to fit our needs

## Databases
Ultimately, data is all zeroes and ones down at the nuts and bolts.
Those zeroes and ones could represent anything, a zero could be off, false, true, orange, green, a, b, c, or anything else. The bits are what we make of them

On our computer we have file systems which Create, read, update, and delete all of our data. It interacts with the firmware for the hard drive to communicate and interpret those ones and zeroes to something usable and meaningful

Both the hard drive and a file system are not databases, even though they store and organize data. They are not databases

Relational Databases are based in mathematical set theory which have relationships but are not required to have them.

We are studying non-relational databases which are bases systems not based in set theory but can still have relationships built into them
![[Drawing 2023-06-27 14.25.38.excalidraw]]
A relational database might look like this, forcing you into forms of normalization \[TAG FORMS OF NORMALIZATION HERE \] 

#### Weaknesses of Relational Databases
- Relational databases are incredibly rigid and structure, so they are very hard and risky to adapt and change. 
- They are also exponentially slowly the more complex relationship get built

#### Modularity of design
Within our Simple persistence phase 1 we need to program intentionally extensible so that as we extend and add more and more to the program. Programming modularity so that we have separate layers built in so extension is easier
1. Data Access Layer
2. Business Logic Layer
3. Service Layer
4. Presentation Layer
5. UI Components
![[IMG_0026.jpg]]
#### Application System
What is it?
- Supports and monitors the execution of an application
- Most things done so far (first 3 quarters) are self contained
- But what we will be looking at now is an application that communicates to a database, web server, network, hardware, everything
![[IMG_0027.jpg]]

