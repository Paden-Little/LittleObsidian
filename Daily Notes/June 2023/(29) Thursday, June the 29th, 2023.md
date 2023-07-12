[[(28) Wednesday, June the 28th, 2023]] #InteractiveWebDev #OpenSourcePlatformsDev #DatabasesII 
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

## Databases II
LOOK INTO PROTOBUFF
### What makes a database a database?
- Implementation of Structure
- Strucutre of data (the data is what we know it is)
- General structure of data that we can understand better
- Restrictions on data to force quality data
- Data accessibility 
- Efficiency 
	- Efficiency of operation / execution
	- Spatial Effeciency
### Serialization
Serialization is the process of encoding and decoding data to improve various aspects of your application

Some serialization processes are better for operational efficiency and some great for spatial efficiency. Typically the better the spatial efficiency the worse the operational efficiency and vice versa.

Java serialization sucks ass

### How to create separation of concerns
![[IMG_0030.jpg]]
The main idea behind separating application layers is to reduce bugs. Whenever you go into add a new feature, or fix an issue, if you have separations you only have to change stuff about one layer instead of potentially having to redo your entire architectures.

Each time you add a new function or class you want a distinct separation with single responsibility. Every function should have only one purpose. 

Between the layers of concern in an application there should be minimal communication between each layer. However, all communications between layers should go through a separate layer called an interface
	The interface is what manages all communications between all the layers. Since — per our diagram — Business layer should communicate between both the resource layer and the presentation layer, we should build interfaces and basically “section out” parts of the business layer to build those communications
