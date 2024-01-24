 
# MongoDB Cheat Sheet for CRUD Operations

## Show all databases:
```bash
show dbs
```

## Switch to a specific database:
```bash
use <database_name>
```

## Show all collections in the current database:
```bash
show collections
```

## Insert a document into a collection:
```bash
db.<collection_name>.insert({ key: value })
```
Example:
```bash
db.users.insert({ name: "John", age: 25, email: "john@example.com" })
```

## Query documents in a collection:
```bash
db.<collection_name>.find({ key: value })
```
Example:
```bash
db.users.find({ name: "John" })
```

## Update documents in a collection:
```bash
db.<collection_name>.update({ key: value }, { $set: { new_key: new_value } })
```
Example:
```bash
db.users.update({ name: "John" }, { $set: { age: 26 } })
```

## Remove documents from a collection:
```bash
db.<collection_name>.remove({ key: value })
```
Example:
```bash
db.users.remove({ name: "John" })
```

## Create an index on a specific field in a collection:
```bash
db.<collection_name>.createIndex({ key: 1 })
```
Example:
```bash
db.users.createIndex({ email: 1 })
```

## Aggregate data in a collection:
```bash
db.<collection_name>.aggregate([ { $group: { _id: "$key", count: { $sum: 1 } } } ])
```

## Drop a collection:
```bash
db.<collection_name>.drop()
```
Example:
```bash
db.users.drop()
```

## Drop a database:
```bash
use <database_name>  # Switch to the database you want to drop
db.dropDatabase()
```
