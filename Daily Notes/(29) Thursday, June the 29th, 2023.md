## Interactive web dev
### Small HTML review
#### `<p>`
Paragraph tag is for small text content
```html
<p>
	Lorem ipsum...
</p>
```

### `<h1>`
Head tag is for titles and sectioning blocks, makes the text bigger and bolder based on which number follow the h. 1-6 where six is the smallest
```html
<h1>Very Large Title</h1>
```
***
## Open Source Platforms Development
### Maven
Maven is a package and build manager for Java. Java by default has no idea of a “Project” without maven. Maven packages our libraries, dependencies, etc.

Whenever programming large projects its important to make ‘Unit Tests’. Unit tests are precoded scripts that will go through your code and do different things to see if it fails or has a bug or whatever

### Testing
#### Assertions
- `assertEquals()`, `assertNotEquals()`, uses ``.equals()
- `assertSame()`, `assertNotSame()`, uses `==`
- `assertNull()`, `assertNotNull()`
- `assertTrue()`, `assertFalse()`
- `assertArrayEquals()`
#### Annotations
- `@BeforeAll`, `@AfterAll`, These two annotations in a test will execute before everything else.
	- If there are multiple `@BeforeAll` it will first execute all of the `@BeforeAll`s top to bottom, then go back to the top and do any non `@BeforeAll`s
- `@BeforeEach()`, `@AfterEach()`, execute this method before/after each normal test method.

