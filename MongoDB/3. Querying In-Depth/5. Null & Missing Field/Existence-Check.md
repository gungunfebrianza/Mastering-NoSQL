Existence Check

The { item : { $exists: false } } query matches documents that do not contain the item field:

db.inventory.find( { item : { $exists: false } } )

The query only returns the document that does not contain the item field.