Pymongo Tutorial
#  Step 1 - Install and import pymongo
import pymongo


# Step 2 - create a mongodb client
conn_str = "mongodb://<username>:<password>@cluster0-shard-00-00.o6ps5.mongodb.net:27017,cluster0-shard-00-01.o6ps5.mongodb.net:27017,cluster0-shard-00-02.o6ps5.mongodb.net:27017/MyFirstDatabase?ssl=true&replicaSet=atlas-bxbdh6-shard-0&authSource=admin&retryWrites=true&w=majority"
try:
    client = pymongo.MongoClient(conn_str)
except Exception:
    print("Error:" + Exception)


#create
#step 3- create a DB
myDb = client["pymongo_demo"]


#step 4 - create a collection
myCollection = myDb["demo_collection"]


#step 5 - Create a document/record
myDoc = {
    
    "name":"Steve",
    "message": "This is pymongo demo"
}


#step-6 insert the document
res = myCollection.insert_one(myDoc)


print(client.list_database_names())


#Step 7: Reading the document
record = myCollection.find_one()


print(record)


#Step 8: Updating the record
query = {
    "message":"This is pymongo demo"
}


new_val = {
    "$set": {"message":"Welcome to coding 101 with Steve"}
}


new_record = myCollection.update_one(query, new_val)
print(new_record)


#Reading the document after updating
record = myCollection.find_one()


print(record)




#Step 9: Delete the Record
query_del = {
    "name": "Steve"
}
record_del = myCollection.delete_one(query_del)


#Reading the document after updating
record = myCollection.find_one()


print(record



