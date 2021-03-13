# mongoDB_UserGuide

#create a databse
use mydb

#check currently selected database:
db

#check your databases list
show dbs

#insert a document
db.movie.insert({"name":"Star Wars"})

#drop a database
db.dropDatabase()

#create a collection
db.createCollection("mycollection")

#drop a collection
db.mycollection.drop()

#insert a document
db.users.insert({
... _id : ObjectId("507f191e810c19729de860ea"),
... title: "MongoDB Overview",
... description: "MongoDB is no sql database",
... tags: ['mongodb', 'database', 'NoSQL'],
... likes: 100
... })


#query documents
db.users.find()


#pretty method
db.users.find().pretty()

#update documents
db.mycol.update({'title':'MongoDB Overview'},{$set:{'title':'New MongoDB Tutorial'}})

#delete document
db.mycol.remove({'title':'MongoDB Overview'})

#projection
db.mycol.find({},{"title":1,_id:0})

#limit
db.users.find({},{"title":1,_id:0}).limit(2)

#sort
db.mycol.find({},{"title":1,_id:0}).sort({"title":-1})
