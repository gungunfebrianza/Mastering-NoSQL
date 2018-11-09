$ne selects the documents where the value of the field is not equal to the specified value. This includes documents that do not contain the field.

Consider the following example:

db.men.find( { qty: { $ne: 20 } } )

This query will select all documents in the inventory collection where the qty field value does not equal 20, including those documents that do not contain the qty field.
