/\*

- We can use "load('path/to/js/file')" function in the mongo shell, to run
- a JavaScript file containing mongodb command for creating a document.
  \*/

try { db.products.insertOne( { item: "card", qty: 15 } ); } catch (e) { print (e); };
try { db.products.insertOne( { item: "card", qty: 16 } ); } catch (e) { print (e); };
try { db.products.insertOne( { item: "card", qty: 17 } ); } catch (e) { print (e); };

This code has been Written By Gun Gun Febrianza
Need Help? Advice? or Ask Question hit me at :
gungunfebrianza@gmail.com

Dont Hesitate to connect with me on social media:
Facebook : www.facebook.com/papabitcoin
Twitter : @daddybitcoin
Instagram : mas.ggun