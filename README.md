# mongodb-developer

## MongoDB Basics
Set up and Atlas cluster, query, create, and analyze your data with MongoDB. Learn about database performance basics, and discover how to get started with creating applications and visualizing your data.

1. What is MongoDB?
  - Collection - an organized store of documents in MongoDB usually with common fields between documents. There can be many collections per database and many documents per collection.
  - Document - a way to organize and store data as a set of field-value pairs.
  - Field - a unique identifier for a datapoint.
  - Value - data related to a given identifier.
  - Replica Set - a few connected machines that store the same data to ensure that if something happens to one of the machines the data will remain intact. Comes from the word replicate - to copy something.
  - Instance - a single machine locally or in the cloud, running a certain software, in our case it is the MongoDB database.
  - Cluster - group of servers that store your data.
  
3. Importing, Exporting, and Querying Data BSON, JSON, importing and exporting data, and Basic Queries
  - How does MongoDB store data?
  - What is JSON?
  - JSON vs. BSON
  ![image](https://user-images.githubusercontent.com/22028539/116987943-1746da00-aca6-11eb-8da0-c970018ea599.png)
  - Importing and Exporting Data
      SRV connection string - a specific format used to establish a connection between your application and a MongoDB instance.
          
          mongodump --uri "mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies"
          mongoexport --uri="mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" --collection=sales --out=sales.json
          mongorestore --uri "mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies"  --drop dump
          mongoimport --uri="mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" --drop sales.json
  
  - Connect To Your Cluster
          - Methods to connect: MongoShell, URI or Compass.

  - Manage Your Cluster From the Command Line Interface
          - Provision and manage clusters with the MongoDB CLI for easier scripting and testing. To get started, create a programmatic API Key for your project
  
  - Binary Import and Export Tools
        1. Replace PASSWORD with the password for the admin user and DATABASE with the name of the database you wish to import/export to your cluster.
        2. mongorestore | creates a new database or adds data to an existing database. By default, mongorestore reads the database dump in the dump/ sub-directory of the current directory; to restore from a different directory, pass in the path to the directory as a final argument.

          mongorestore --uri mongodb+srv://adm:<PASSWORD>@cluster0.vvo6a.mongodb.net 
          mongodump | creates a binary export of the contents of a database
          mongodump --uri mongodb+srv://adm:<PASSWORD>@cluster0.vvo6a.mongodb.net/<DATABASE> 

  - Data Import and Export Tools
    Replace PASSWORD with the password for the admin user, DATABASE with the name of the database you wish to import/export to your cluster, and COLLECTION with the name of the collection you wish to import/export to your cluster. Replace FILETYPE with "json" or "csv" to specify the file type. Where applicable, replace FILENAME with the location and name of the output file (for export) or data source (for import).

        mongoimport | imports content from an Extended JSON, CSV, or TSV export
        mongoimport --uri mongodb+srv://adm:<PASSWORD>@cluster0.vvo6a.mongodb.net/<DATABASE> --collection <COLLECTION> --type <FILETYPE> --file <FILENAME>
        mongoexport | produces a JSON or CSV export of data stored in a MongoDB instance
        mongoexport --uri mongodb+srv://adm:<PASSWORD>@cluster0.vvo6a.mongodb.net/<DATABASE> --collection <COLLECTION> --type <FILETYPE> --out <FILENAME>

- Set Up Diagnostics
  Replace PASSWORD with the password for the admin user.

        mongostat | provides a quick overview of the status of a currently running mongod or mongos instance
        mongostat --uri mongodb+srv://adm:<PASSWORD>@cluster0.vvo6a.mongodb.net 
        mongotop | tracks the amount of time a MongoDB instance spends reading and writing data
        mongotop --uri mongodb+srv://adm:<PASSWORD>@cluster0.vvo6a.mongodb.net 
  
  - Data Explorer (Using GUI and CLI):
          - Namespace: The concatenation of the database name and collection name is called a namespace.

TODO: Deploy a definitive Atlas MongoDB cluster and import/export json/bson data files on it using GUI/CLI
    
  - Find Command
  - The mongo shell


4. Creating and Manipulating Documents Insert, Update, and Delete operations
5. Advanced CRUD Operations Query operators: element operators, logical operators, array operators, and the regex operator
6. Indexing and Aggregation Pipeline aggregation, indexes, data modeling
7. Next Steps Atlas Data Explorer, Performance Advisor, Charts, Realm, Compass


## INTRODUCTORE
### New Features and Tools in MongoDB 3.6
This is a continuing education course on the upcoming 3.6 release of MongoDB. In a series of what will be approximately 9 modules, we will introduce the main features of 3.6 in detail.

### New Features and Tools in MongoDB 4.0
This is a continuing education course that covers new features and tools released with MongoDB 4.0. In a series of 9 chapters, we will explore all the new functionality available with 4.0 including recently released features in Atlas, Compass, OpsManager and the BI Connector.

## New Features and Tools in MongoDB 4.2
This is a continuing education course that covers new features and tools released with MongoDB 4.2. In a series of 7 chapters, we will explore all the new functionality available with 4.2 including recently released features in Atlas, in Charts, Cloud & OpsManager and in the Enterprise Tools.

### MongoDB for SQL Pros
Helping users with RDBMS and SQL knowledge learn MongoDB.

### The MongoDB Aggregation Framework
Fundamentals of the powerful MongoDB Aggregation Framework: data transformation, data science, reducing data over the wire, views.

## INTERMEDIATE
### MongoDB Performance
Learn how to optimize the performance of your MongoDB deployment. This course will cover how to use best practices for achieving performance at scale in a MongoDB system.

### MongoDB for Java Developers
Learn everything you need to know to get started building a MongoDB-based app in Java.

### MongoDB for Javascript Developers
Learn everything you need to know to get started building a MongoDB-based app in Node.js.

### MongoDB for .NET Developers
Learn everything you need to know to get started building a MongoDB-based app in C#.

### MongoDB for Python Developers
Learn everything you need to know to get started building a MongoDB-based app in Python.

## ADVANCED
### Data Modeling
How to model data and create schemas for MongoDB
