Search for a Phrase

To match the exact phrase as a single term, escape the quotes.

The following query searches for the phrase coffee shop:
db.articles.find( { $text: { $search: "\"coffee shop\"" } } )

This query returns documents that contain the phrase coffee shop:
{ "_id" : 2, "subject" : "Coffee Shopping", "author" : "efg", "views" : 5 }

