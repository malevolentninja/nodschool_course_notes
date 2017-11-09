# UPDATE

Update a document in the users collection 
- Database name will be accessible via process.argv[2]
- For this lesson assume that the username property is unique

Solution: 
```sh
var mongo = require('mongodb').MongoClient

var url = 'mongodb://localhost:27017/' + process.argv[2]
mongo.connect(url, function(err, db) {
  if (err) throw err
  var collection = db.collection('users')
  collection.update({
    username: 'tinatime'
  }, {
    $set: {
      age: 40
    }
  }, function(err) {
    if (err) throw err
    db.close()
  })
})
```
