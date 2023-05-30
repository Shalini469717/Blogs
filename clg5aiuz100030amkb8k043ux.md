---
title: "CRUD operations in MongoDB"
seoTitle: "MongoDB crud operations"
datePublished: Thu Apr 06 2023 15:46:10 GMT+0000 (Coordinated Universal Time)
cuid: clg5aiuz100030amkb8k043ux
slug: crud-operations-in-mongodb
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1681236973759/adedc76d-cfdf-4299-8cd1-5d316f8dc355.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1680795953593/348d3d83-7c8a-49f5-aafd-bf7d15db42c0.png
tags: programming-blogs, web-development, mongodb, backend, webdev

---

In this blog I will be covering the CRUD operations on a database in MongoDB with examples.

Instead of records, MongoDB has `documents`. You have `collections` instead of tables.  
Let us see how to perform CRUD operations in MongoDB.

Use `show dbs` to show the databases. `use databseName` opens the database if it already exists else it creates a new database.

You can create a collection by using `db.createCollection("Collection Name")` . You can use `show collections` to view the collections in the database.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680685962748/b476bd73-07c5-4a98-9051-9e8ecbb659fa.png align="center")

## Create/save documents in a collection

InsertOne: Used to insert a single document into the collection. `db.collectionName.insertOne(document)`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680686263986/065546e0-24a4-41d8-a712-4697160e41d4.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680686530096/0b2399f0-c76f-4a87-b63a-c0c1a268bde7.png align="center")

InsertMany: Used to insert many documents into the collection.

`db.collectionName.insertMany([document1, document2])`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680686723394/e15e25a7-e5d7-4ee4-bba5-7c66da093c07.png align="center")

## Finding a document

`db.collectionName.findOne()` returns the first document in the collection.

`db.collectionName.find()` returns all the documents in the collection.

Query Operators

`$eq` - equal to

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680687100346/76f5b8c2-3d5c-4a2c-993f-59613d6668de.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680687166852/b8ef23eb-22ea-4081-825f-ec43ba34a456.png align="center")

`$gt` - greater than

`$gte` - greater than or equal to

`$lt` - less than

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680687275715/838b2ed2-cf86-42ab-87f9-a75f9eca4acb.png align="center")

`$in` - check if the value is there

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680687508899/be9708ad-10a2-44fe-9d61-570bfcb29cfd.png align="center")

`$and` - and operation between the conditions

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680687627352/74ea368d-9de4-4336-b54f-4e42b06f2f33.png align="center")

The `$all` operator selects the documents where the value of a field is an array that contains all the specified elements.

`$size` - checks the size

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680688064427/d52f9472-d815-4bf8-b52c-9e921c412473.png align="center")

## Update documents of a collection

It can be done using `$set` operator. `updateOne` updates the first document in the resulting search of the collection. `updateMany` updates all the documents matching the search conditions.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680794869209/14423d96-1803-42fc-a7de-37de62629578.png align="center")

other operators:

`$set` - assign new value and change the existing value.  
`$inc` - increment  
`$rename` - used to rename the field.  
`$unset` - remove any field from the document.

  
Array update operators  
`$add_to_set` - won't add if it is already present.  
`$push` - pushes into the set  
`$pop` - can remove from beginning/ending  
`$pull` - remove using the name  
`$pullAll` - removes all

![](https://lh4.googleusercontent.com/jHVHb1iklw8HDZwnBGeIO4GOOsS0e9MU5ZP2GHs7WF--pE4rlH6Gna9sBCluju2ze_EDmBiWxo8wSkm_Z1OPr9npcQ1cwPtnQ8-3zsjJWAo9uRD82qjlS3S9R9GKcyxfOamslMC6fCOJetVJpWMi6A align="left")

![](https://lh6.googleusercontent.com/7ubW1NtC4loHoGQhWKjk9YkCKSqrrqxtcOSnqAvWb4OptHpzg5KcOBmepUnpff5d_i_Gguas8J4V4sJFkFbmVlSBIFoUGqVoVKsT0-Xk5Kx29dIdQ6ImhdsJj1tl1fMAxw9OqAU9I0Nibr88z14YzA align="left")

![](https://lh3.googleusercontent.com/proaoSrtU7Ym7gBqhcUZNoF9W31KIjZ7YId_1GvJEXqPE4yXgBwbDqKzo2ontxfvt4n7xORuDEzSmAjQRu5IJ3t6n_yLzspbSiF1soSn2k9cV7QyFex1uyGWuJEqJdfYCFgymaWbVa2po6JKWRfcsQ align="left")

# Delete documents of a collection

`deleteOne(condition)` - used to delete the topmost result

`deleteMany(condition)` - used to delete the documents that match the condition

![](https://lh6.googleusercontent.com/fUqc8_PVzASHOByea_CUZlZ2DZMJiNKLoAk4R6qAzvB2MTqGymp8BvuGX-bMxivUIfDxS5s24lql7V_FXLH7x3GhzdnRZPFJ1rRoFAyqXR2c3RzsV_bxBkBHsngJWecICfY9QVk7rNZx4l-OJxAb1A align="left")

## Drop database and collection

`db.dropDatabase()` - used to drop current database

`db.collectionName.drop()` - used to drop collection

![](https://lh4.googleusercontent.com/TkaQPt7CLi9l9R5rOzZh0-u0s6J7txNqr9dR2Vs-weHO2feHw4KqaSalHnc-UgGfDxPakXJfPgQbJDYsnC4zle1-rINoyATdMfbN2PdYW2OWbJ4DiwQ5m6X1Kdzgg3w76mbasCvGGLGlbcvcZnfpeQ align="left")

![](https://lh3.googleusercontent.com/HK-xSBOnC5Aj0-9Bl4b50AshBizy_147EbyYxwbAC934eOPnqx-V6twO_uKWenRQekKdaq8EU7IFtqBammlrAUf16GpHArlw1daWns0qds8qintpPpHqQCDvpZLr9hL0dFhLZ2GtCfVJ4taiYUc8dg align="left")

Thank you for reading the blog. I was revising MongoDB and dropped references from my notes. Feel free to comment in case of any suggestions or issues. Feedback is always welcomed!