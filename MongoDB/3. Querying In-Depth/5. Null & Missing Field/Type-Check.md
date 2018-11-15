Type Check

The { item : { $type: 10 } } query matches only documents that contain the item field whose value is null; i.e. the value of the item field is of BSON Type Null (type number 10) :

db.inventory.find( { item : { $type: 10 } } )

https://docs.mongodb.com/manual/reference/bson-types/