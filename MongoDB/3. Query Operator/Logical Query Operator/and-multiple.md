db.men.find( {
    $and : [
        { $or : [ { wallet : 3000 }, { wallet : 5000 } ] },
        { $or : [ { age : 20 }, { age : { $lt : 30 } } ] }
    ]
} )