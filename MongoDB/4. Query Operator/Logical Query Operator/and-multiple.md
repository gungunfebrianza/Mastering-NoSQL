db.men.find( {
$and : [
{ $or : [ { wallet : 3000 }, { wallet : 5000 } ] },
{ $or : [ { age : 20 }, { age : { $lt : 30 } } ] }
]
} )

This code has been Written By Gun Gun Febrianza
Need Help? Advice? or Ask Question hit me at :
gungunfebrianza@gmail.com

Dont Hesitate to connect with me on social media:
Facebook : www.facebook.com/papabitcoin
Twitter : @daddybitcoin
Instagram : mas.ggun
