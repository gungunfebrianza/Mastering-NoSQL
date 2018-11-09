Element Match

Given the following documents in the scores collection:

{ _id: 1, results: [ 82, 85, 88 ] }
{ _id: 2, results: [ 75, 88, 89 ] }

The following query matches only those documents where the results array contains at least one element that is both greater than or equal to 80 and is less than 85.

db.scores.find(
   { results: { $elemMatch: { $gte: 80, $lt: 85 } } }
)

The query returns the following document since the element 82 is both greater than or equal to 80 and is less than 85

{ "_id" : 1, "results" : [ 82, 85, 88 ] }

