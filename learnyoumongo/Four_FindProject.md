# Find Project

Learn how to search for documents but only fetch the fields we need. 
Also known as projection in MongoDB.

Use the parrots collection from the database named learnyoumongo to 
- find all documents where age is greater than the first argument passed to your script
- only want the name and age properties
- Using console.log, print the documents to stdout.

## Full Solution: 

```sh
var mongo = require('mongodb').MongoClient
var age = process.argv[2]

var url = 'mongodb://localhost:27017/learnyoumongo'

mongo.connect(url, function(err, db) {
  if (err) throw err
  var parrots = db.collection('parrots')
  parrots.find({
    age: {
      $gt: +age
    }
  }, {
    name: 1
  , age: 1
  , _id: 0
  }).toArray(function(err, docs) {
    if (err) throw err
    console.log(docs)
    db.close()
  })
})

```
