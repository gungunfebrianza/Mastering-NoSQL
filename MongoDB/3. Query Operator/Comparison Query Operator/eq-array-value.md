The following example queries the inventory collection to select all documents where the tags array equals exactly the specified array or the tags array contains an element that equals the array [ "A", "B" ].

db.men.find( { tags: { $eq: [ "A", "B" ] } } )

The query is equivalent to:

db.men.find( { tags: [ "A", "B" ] } )

Both queries match the following documents:

{ \_id: 3, item: { name: "ij", code: "456" }, qty: 25, tags: [ "A", "B" ] }
{ \_id: 5, item: { name: "mn", code: "000" }, qty: 20, tags: [ [ "A", "B" ], "C" ] }
