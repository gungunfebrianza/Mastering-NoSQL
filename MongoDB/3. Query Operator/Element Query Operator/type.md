Querying by Data Type

The addressBook contains addresses and zipcodes, where zipCode has string, int, double, and long values:

db.addressBook.insertMany(
   [
      { "_id" : 1, address : "2030 Martian Way", zipCode : "90698345" },
      { "_id" : 2, address: "156 Lunar Place", zipCode : 43339374 },
      { "_id" : 3, address : "2324 Pluto Place", zipCode: NumberLong(3921412) },
      { "_id" : 4, address : "55 Saturn Ring" , zipCode : NumberInt(88602117) }
   ]
)

The following queries return all documents where zipCode is the BSON type string:

db.addressBook.find( { "zipCode" : { $type : 2 } } ); //(number 2 mean string)
db.addressBook.find( { "zipCode" : { $type : "string" } } );

These queries return:

{ "_id" : 1, "address" : "2030 Martian Way", "zipCode" : "90698345" }

