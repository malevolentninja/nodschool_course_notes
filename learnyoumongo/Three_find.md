# FIND

The url is mongodb://localhost:27017/learnyoumongo as the database is named learnyoumongo

Use the ```sh parrots``` collection to find all documents where 
- age is greater than the first argument passed to your script

Using console.log, print the documents to ```sh stdout```

### Connecting the database:
```sh
var mongo = require('mongodb').MongoClient
mongo.connect(url, function(err, db) {
  // db gives access to the database
})
```
### Access the arguments, use the process.argv 
```sh
var age = process.argv[2]
```

### The url variable: 
```sh
var url = mongodb://localhost:27017/learnyoumongo'
```

### close program:
```sh
db.close()
```

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
  }).toArray(function(err, docs) {
    if (err) throw err
    console.log(docs)
    db.close()
  })
})

```
