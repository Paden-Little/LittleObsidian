[[(19) Wednesday, July the 19th, 2023]] #InteractiveWebDev #OpenSourcePlatformsDev #DatabasesII 
## Interactive Web Dev
### Web servers
A web server is an application that responds to (typically requests) and gives a response. 
#### Setting up a webserver
To set up a node project (webserver) run `npm init`  in the directory you want to store the project. It will ask a bunch of configuration questions. 
#### Building an API
API's need a BUNCH of stuff to work. And we definitely don't want to build all of that ourselves. So we are going to use a framework. A framework is a collection of a bunch of packages surrounded by a common theme. For this we will be using Express.js.
### Express.js
Express.js is a frame work for building webserver. It has tools for APIs, HTTP requests, routing, and more. 

## Databases
### Indexes
Indexes assign numbers to elements. indexing is interesting
To create an index do this
```JS
db.restaurant.createIndex({
	borough: 1
})
```
- indexing will ask what data to index things on - `borough:`
- This will create an index, ordered by borough, ascending by 1
Indexes somewhat more efficient then typical hashing.
Indexes is most useful when caching is least useful