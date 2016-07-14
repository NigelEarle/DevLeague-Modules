*Before starting run the commands `brew doctor` and then `brew update`*

*Unix Users please install using the [docs](http://docs.mongodb.org/manual/administration/install-on-linux/)*

# Install Mongodb via Homebrew
`$ brew install mongodb`

Once brew is done installing, take note of the Caveats section that is printed to your console. Just like what we did previously for postgres it might be best to [create a symlink then two aliases to start and stop the mongo progress](https://gist.github.com/sgnl/6e1fac7f698953e9df59).

- Start your mongodb service
- Connect to your mongodb server with the command `$ mongo`
- Enter the command: `$ use local`

**Your prompt should look something like this:**
```
MongoDB shell version: 3.0.4
connecting to: test
>
```

## REPL
Enter `1 + 1`, you'll notice that the mongodb-cli will evaluate to `2`. This means that you are in MongoShell (a Javascript REPL). To further illustrate this go ahead and declare a new variable named `person` which is an object literal with a single property of `name` and set it to your name. Enter the command `person` to recall your object that you just created. You can do `FOR` loops and even declare and call functions.

## Help Command
`$ help` will show a menu of help commands.

## Create a Database
- In a SQL database we have to create a database we have to run a query that looks like this:

```sql
CREATE DATABASE DB_NAME_HERE;
```

- In MongoDB we can issue the `use` command with the databse name as its only parameter.

To create a Database named `mongodb_intro`, to create it we will run this command `$ use mongodb_intro`. Now we are using a database, we can use db methods. To see what methods are available you can refer to the help command: `$ db.help();`

Forget what database you're using? `$ db.getName();`

## Create a Collection, Inserting a Document, Querying for Data
- In a SQL database we have **Tables** but in MongoDB we have **Collections**.
- In a SQL database, **Tables** contain **Rows** of data. In MongoDB **Collections** contain **Documents**.

When we run the command `$ db.getCollectionNames();` you should see an empty array, `[]`, we don't have our own collection so lets create a collection named `users`... there are two ways to do it. Let's do **both**.

**Creating a collection explicitly and inserting our `person` object (#1)**
```javascript
// create collection
$ db.createCollection("users"); //-> { "ok" : 1 }

// insert our data by calling db.collectionName.insert method
$ db.users.insert(person);      //-> WriteResult({ "nInserted" : 1 })

// Query the database for Documents
$ db.users.find();              //-> prints all documents found in the users collection, should only be one object
```

*before we continue we will need to drop the `users` collection*

`$ db.users.drop();             //-> true`

**Creating a collection implicityly by inserting data (#2)**
```javascript
$ db.users.insert(person);     //-> WriteResult({ "nInserted" : 1 })
$ db.users.find();             //-> prints all documents found in the users collection, should only be one object
```

### WAIT A MINUTE
Do you see a difference between the two series of operations? Step #2 doesn't have a command that explicitly creates a collection yet a collection of `users` was created anyway. Also, you may have noticed that we haven't defined any **Columns** nor specified **Data Types** for these non-present columns. Crazy right? Basically MongoDB just takes a Javascript object, you tell it where you want to store it (Collection) and Mongo says, "Got the Data and I got the Collection to store it to, Thanks!".

### Insert more data but with varying properties
MongoDB is very relaxed compared to SQL Databases.

Take some time to create another object to save to the `users` collections and instead of a name property, make up a few properties and then insert it into the collection then query your collection for the data.

> Like Honey Badger, MongoDB don't [care](https://www.youtube.com/watch?v=4r7wHMg5Yjg)

## Explore
- Can you find the `db.collection` Method for Modifying a document that already exists?
- Does MongoDB have aggregate methods?
- How is "Indexing" done in MongoDB
- What is "Sharding"?
- Does Mongo provide a way to migrate your data across multiple servers?

# References
[MongoDB Shell](http://docs.mongodb.org/manual/reference/mongo-shell/)

[MongoDB Shell Methods](http://docs.mongodb.org/manual/reference/method/)

[MongoDB Cursor](http://docs.mongodb.org/manual/core/cursors/)
