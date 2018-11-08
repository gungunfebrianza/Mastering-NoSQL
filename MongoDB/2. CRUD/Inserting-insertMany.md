try {
db.products.insertMany( [
{ item: "card", qty: 15 },
{ item: "envelope", qty: 20 },
{ item: "stamps" , qty: 30 }
] );
} catch (e) {
print (e);
}
