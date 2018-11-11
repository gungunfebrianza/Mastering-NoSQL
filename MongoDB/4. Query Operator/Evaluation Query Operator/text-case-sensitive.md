Perform Case Sensitive Search

Changed in version 3.2.

To enable case sensitive search, specify $caseSensitive: true. Specifying $caseSensitive: true may impact performance.
Case Sensitive Search for a Term

The following query performs a case sensitive search for the term Coffee:

db.articles.find( { $text: { $search: "Coffee", $caseSensitive: true } } )

The search matches just the document:

{ "_id" : 2, "subject" : "Coffee Shopping", "author" : "efg", "views" : 5 }
