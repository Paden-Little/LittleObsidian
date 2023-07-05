## Interactive Web Dev
#### Arrow Notation of Function Declaration
- The arrow `=>` means “from something do something” and the something is a function even if it doesn’t have the `function` keyword
- Arrow Notation tells a function to execute asynchronously
- `fetch()` is a method used for API calls, you put in a URL, and it returns a promise 
	- A promise says I don’t have the data yet, but I promise you when ever I get it ill let you know
	- The way you fulfill that response is using the promises built in `then()` function
```JavaScript
var promiseOfResponse = fetch(”https:websiteAPICall”)

promiseOfResponse.then(starWarsStuff)

function starWarsStuff(starWarsStuff){
	console.log(starWarsStuff)
}
```
- Instead of doing this long winded way of doing it, there’s a faster way using our Asynch arrow 
```Javascript
fetch(“https://swapi.dev/api/people/2”).then(response) => {
	response.json().then(data) => {
		console.log(data)
	}
}
```
## Open Source Development Platforms
#### Maven
Maven is basically java projects with a little extra stuff
Maven adds a file structure to the java for both our source code and our executable builds
Maven also adds a section called pom.xml which stands for project object model, which stores properties, dependencies, etc for the project.