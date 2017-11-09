# INSERT

- Connect to MongoDB on port 27017.
- You should connect to the database named learnyoumongo
- insert a document into the docs collection
- hould be a json document with the following properties:
     - firstName: the first argument to the lesson
     - lastName: the second argument to the lesson
- console.log to print out the object used to create the document
- JSON.stringify to convert to JSON



Solution:
```sh
var mongo = require('mongodb').MongoClient

var firstName = process.argv[2]
var lastName = process.argv[3]
var doc = {
  firstName: firstName
, lastName: lastName
}

var url = 'mongodb://localhost:27017/learnyoumongo'
mongo.connect(url, function(err, db) {
  if (err) throw err
  var collection = db.collection('docs')
  collection.insert(doc, function(err, data) {
    if (err) throw err
    console.log(JSON.stringify(doc))
    db.close()
  })
})

```
