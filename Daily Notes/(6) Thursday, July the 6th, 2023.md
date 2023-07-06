## Interactive Web Dev
### What is node?
Node is basically just the V8 engine from the browser to a desktop service. 

## Open Source Platforms Development
### JSON in Java


## Databases
#### Aspects of Databases
- Structure
- CRUD
- Effeciency

#### How does serialization effect Database efficiency 
- Serialization helps data integrity
	- Creates consistent data
	- Won’t be overwritten deleted or edited without our permission
- Serialization of data helps consistency of interpretation, makes it so we know how our data is going to be always
- Serialization gives different amounts of efficiency of operational and spatial
- USE PROTOBUFF
- Serialization generally makes data bigger thus lowering spatial efficiency
- The same non-serialized file takes about 25~ bytes while java serialized data takes up about 150~ bytes for the same data

#### Data Structures
- A set of rules and structures for governing data
##### Arrays
Arrays are the most basic form of data structures. It’s a set of indexed elements of the same type. Strings are arrays of characters
- True arrays are required to be of the same primitive type. But why?
	- Primitive types have capped size. So whenever an array is declared it takes the number of elements multiplied by the size of the primitive its storing.
	- The data in bits is stored back to back 0 index data then 1 index data and so on till the end. This is called Localized memory

##### Hash maps
Hash maps are sets of key-value pairs. The key describe what the data is while the value is a hash.

###### What is a hash?
- A hash is an algorithm that changes data to another form that is non-reversible. 
- For example:
	- `Password1` could be turned into `3ab6c908` after hashed. 
	- A hash cannot be reversed, the only way to figure out what it is is to put in the original data that went in to be hashed, and compare the stored hash to the created hash
###### How do hash maps work?
