Exclude Documents That Contain a Term

A negated term is a term that is prefixed by a minus sign -. If you negate a term, the $text operator will exclude the documents that contain those terms from the results.

The following example searches for documents that contain the words coffee but do not contain the term shop, or more precisely the stemmed version of the words:

db.articles.find( { $text: { $search: "coffee -shop" } } )

The query returns the following documents:

{ "\_id" : 7, "subject" : "coffee and cream", "author" : "efg", "views" : 10 }
{ "\_id" : 1, "subject" : "coffee", "author" : "xyz", "views" : 50 }
