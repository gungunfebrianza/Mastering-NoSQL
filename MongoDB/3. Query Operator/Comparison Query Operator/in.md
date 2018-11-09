Use the $in Operator to Match Values

db.men.find( { qty: { $in: [ 5, 15 ] } } )

This query selects all documents in the inventory collection where the qty field value is either 5 or 15. Although you can express this query using the $or operator, choose the $in operator rather than the $or operator when performing equality checks on the same field.

This code has been Written By Gun Gun Febrianza
Need Help? Advice? or Ask Question hit me at :
gungunfebrianza@gmail.com

Dont Hesitate to connect with me on social media:
Facebook : www.facebook.com/papabitcoin
Twitter : @daddybitcoin
Instagram : mas.ggun