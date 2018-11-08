The following example queries the inventory collection to select all documents where the value of the name field in the item document equals "ab". To specify a condition on a field in an embedded document, use the dot notation.

db.men.find({ 'item.name': { $eq: 'ab' } }).pretty()

The query is equivalent to:

db.men.find( { "item.name": "ab" } )

Both queries match the following document:

{ _id: 1, item: { name: "ab", code: "123" }, qty: 15, tags: [ "A", "B", "C" ] }



/* Example Script :
{ _id: 1, item: { name: "ab", code: "123" }, qty: 15, tags: ["A", "B", "C"] }
{ _id: 2, item: { name: "cd", code: "123" }, qty: 20, tags: ["B"] }
{ _id: 3, item: { name: "ij", code: "456" }, qty: 25, tags: ["A", "B"] }
{ _id: 4, item: { name: "xy", code: "456" }, qty: 30, tags: ["B", "A"] }
{ _id: 5, item: { name: "mn", code: "000" }, qty: 20, tags: [["A", "B"], "C"] } */