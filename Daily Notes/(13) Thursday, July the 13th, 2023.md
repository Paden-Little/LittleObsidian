[[(12) Wednesday, July the 12th, 2023]] #InteractiveWebDev #OpenSourcePlatformsDev #DatabasesII #Regex #NodeJS 
## Interactive Web Dev
### Creating CLIs in Node
Node has a way to build CLI using 'createInterface'
```JS
const rl = readline.createInterface(
	{
		input: process.stdln,
		out: process.stdout
	}
);
```
Its an asynchronous function where we have to explicitly say whether we want the program to wait with `await` for the user input before continuing execution or continue execution with `async`. However this asynchronous function does not use promises like fetch does, it uses callbacks
```js
rl.question('what do you think of Node.js?', (answer) =>{
	console.log('Thank you for your valuable feedback: ' ${answer});
	rl.close();
})
```

## Open source platforms development
### Regex
Groups within regex are NOT zero indexed, they are 1 indexed.