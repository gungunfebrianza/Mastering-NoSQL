The following example queries the inventory collection to select all documents where the tags array contains an element with the value "B" [1]:

db.men.find( { tags: { $eq: "B" } } )

The query is equivalent to:

db.men.find( { tags: "B" } )

Both queries match the following documents:

{ _id: 1, item: { name: "ab", code: "123" }, qty: 15, tags: [ "A", "B", "C" ] }
{ _id: 2, item: { name: "cd", code: "123" }, qty: 20, tags: [ "B" ] }
{ _id: 3, item: { name: "ij", code: "456" }, qty: 25, tags: [ "A", "B" ] }
{ _id: 4, item: { name: "xy", code: "456" }, qty: 30, tags: [ "B", "A" ] }