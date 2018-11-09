Match Any of the Search Terms

If the search string is a space-delimited string, $text operator performs a logical OR search on each term and returns documents that contains any of the terms.

The following query specifies a $search string of three terms delimited by space, "bake coffee cake":

db.articles.find( { $text: { $search: "bake coffee cake" } } )

This query returns documents that contain either bake or coffee or cake in the indexed subject field, or more precisely, the stemmed version of these words:

{ "id" : 2, "subject" : "Coffee Shopping", "author" : "efg", "views" : 5 }
{ "id" : 7, "subject" : "coffee and cream", "author" : "efg", "views" : 10 }
{ "id" : 1, "subject" : "coffee", "author" : "xyz", "views" : 50 }
{ "id" : 3, "subject" : "Baking a cake", "author" : "abc", "views" : 90 }
{ "id" : 4, "subject" : "baking", "author" : "xyz", "views" : 100 }
