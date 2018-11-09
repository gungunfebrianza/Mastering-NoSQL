db.men.find({ $and: [ { wallet: { $ne: 3000 } }, { wallet: { $exists: true } } ] })
