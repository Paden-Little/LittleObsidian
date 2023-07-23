[[(17) Monday, July the 17th, 2023]] #DatabasesII #MongoDB 
## Databases
### MongoDB
Sum, Average, and Count are all aggregation operations. An aggregation is a grouping and combination of things. 
```JS
db.menu.aggregate([
	{$group: {
		_id: "$type",
		averagePrice: {$avg: "$price"}
	}},
	{$group: {
		_id: null,
		totalAverage: {$sum: "$averagePrice"}
	}}
])
```
We are going into the menu and adding together the average price of a drink, entrée, and side. 

#### Deleting items
```JS
db.menu.deleteOne({name: "Papa's Favourite"})
```
To delete something you have to pass a search object into the method, `deleteOne` will delete the first instance it finds
```JS
db.menu.deleteMany({name: "Papa's Favourite"})
```
This will delete anything and everything which name is equal to "Papa's Favourite". 

#### Updating items
```JS
db.menu.updateOne(
	{name: "Eggplant (raw)"},
	{$set: {ingredients: [
		{name: "Eggplant", cost: 2},
		{name: "Tomato Jam", cost: 0.5}
	]}}
)
```
The first parameter is the search object, while the second is the object which will tell it how to update the entry. It also has an `updateMany` version.

#### Now lets look at the average profit margin for the entrees
```JS
db.menu.aggregate([
	{$match: {type: "Entree"}}, //We match on a search object
	{$group: { //Now we group all ids, then average the price of all entrees
		_id: null,
		averagePrice: {$avg: "$price"}
	}}
]
)
```
This will average is all, however we can add an unwind to get the ingredients
```JS
db.menu.aggregate([
	{$match: {type: "Entree"}},
	{$unwind: "$ingredients"}, //Adding this 
	{$group: { 
		_id: null,
		totalCost: {$sum: "$ingredients.cost"} //And changing this
	}}
]
)
```
This will now add the cost of all of the ingredients for each entrée, and print the id and the total cost
```JS
db.menu.aggregate([
	{$match: {type: "Entree"}},
	{$unwind: "$ingredients"},  
	{$group: { 
		_id: null,
		totalCost: {$sum: "$ingredients.cost"},
		price: {$avg: "$price"}
	}},
	{$project: {
		profitMargin: {$subtract: ["$price", "$totalCost"]}}
	}
]
)
```

