Querying by Multiple Data Type

The grades collection contains names and averages, where classAverage has string, int, and double values:

db.grades.insertMany(
   [
      { "_id" : 1, name : "Alice King" , classAverage : 87.333333333333333 },
      { "_id" : 2, name : "Bob Jenkins", classAverage : "83.52" },
      { "_id" : 3, name : "Cathy Hart", classAverage: "94.06" },
      { "_id" : 4, name : "Drew Williams" , classAverage : 93 }
   ]
)

The following queries return all documents where classAverage is the BSON type string or double. The first query uses numeric aliases while the second query uses string aliases.

db.grades.find( { "classAverage" : { $type : [ 2 , 1 ] } } );
db.grades.find( { "classAverage" : { $type : [ "string" , "double" ] } } );

These queries return the following documents:

{ "_id" : 1, name : "Alice King" , classAverage : 87.333333333333333 }
{ "_id" : 2, name : "Bob Jenkins", classAverage : "83.52" }
{ "_id" : 3, name : "Cathy Hart", classAverage: "94.06" }

