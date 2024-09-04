# IBM - Node.js & MongoDB Developing Back-end Database Applications
IBM - Node.js & MongoDB Developing Back-end Database Applications

* IBM Data Engineering [IBM]( https://github.com/jkaewprateep/Portfolio/blob/main/Coursera%20H4HDKPEV6VVW.pdf ) </br>
* IBM Back-end JavaScript Developer [IBM]( https://github.com/jkaewprateep/Portfolio/blob/main/Coursera%208BUX52L749RU.pdf ) </br>
* IBM Data Warehouse Engineer [IBM]( https://github.com/jkaewprateep/Portfolio/blob/main/Coursera%204K7JZCI2I9XO.pdf ) </br>
* Meta Back-End Developer [META]( https://github.com/jkaewprateep/Portfolio/blob/main/Coursera%20FANPMLCYFSZ2.pdf ) </br>
* Meta Database Engineer [META]( https://github.com/jkaewprateep/Portfolio/blob/main/Coursera%20VVUULL2PK26V.pdf ) </br>
* SQL (Advance) [HackerRank]( https://www.hackerrank.com/certificates/f225fa371510 ) </br>
* REST API (Immediate) [HackerRank]( https://www.hackerrank.com/certificates/6e02a6153c0f ) </br>
* .NET FullStack Developer [Board]( https://github.com/jkaewprateep/Portfolio/blob/main/Coursera%206DRYK7YS79ZT.pdf ) </br>

<p align="center" width="100%">
    <img width="47%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/Node.js%20%26%20MongoDB%20Developing%20Back-end%20Database%20Applications-instructors.png">
    <img width="17.63%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/kid_30.jpg">
    <img width="10.48%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/kid_38.jpg"> </br>
    <b> Pictures from the Internet </b> </br>
</p>

## app.js ##

```
const mongoose = require('mongoose');
const Employee = require('./employee');

const uri =  "mongodb://root:MjI4MjMtamthZXdw@localhost:27017";

mongoose.connect(uri,{'dbName':'employeeDB'});

Employee.find().then((data)=>{
            console.log(data);
            mongoose.connection.close()
})
```

## app_delete.js ##

```
const mongoose = require('mongoose');
const Schema = mongoose.Schema;

const Employee = require('./employee');

const uri =  "mongodb://root:MjI4MjMtamthZXdw@localhost:27017";

mongoose.connect(uri,{'dbName':'employeeDB'})
    .then(() => {
        console.log("Connected to MongoDB");

        // Delete one record from employees
        return Employee.deleteOne({ age: { $lt: 30 }, location: "New York" });
    })
    .then((deleteOneResult) => {
        console.log("Deleted document for deleteOne:", deleteOneResult);

        // Delete many records from employees
        return Employee.deleteMany({ emp_name: { $regex: "R" } });
    })
    .then((deleteManyResult) => {
        console.log("Deleted documents for deleteMany:", deleteManyResult);
    })
    .catch((error) => {
        console.error("Error:", error);
    })
    .finally(() => {
        mongoose.connection.close(); // Close the MongoDB connection
    });
```

## app_insertMany.js ##

```
const mongoose = require('mongoose');
const Schema = mongoose.Schema;
const Employee = require('./employee');

const uri =  "mongodb://root:MjI4MjMtamthZXdw@localhost:27017";


mongoose.connect(uri,{'dbName':'employeeDB'})
    .then(() => {
        console.log("Connected to MongoDB");

        // insertMany records into employee
        return Employee.insertMany([
            { "emp_name": "Ray Renolds", "age": 32, "location": "Austin", "email": "rayr@somewhere.com" },
            { "emp_name": "Matt Aniston", "age": 25, "location": "Houston", "email": "matta@somewhere.com" },
            { "emp_name": "Monica Perry", "age": 23, "location": "New Jersey", "email": "monicap@somewhere.com" },
            { "emp_name": "Rachel Tribbiani", "age": 28, "location": "Boston", "email": "rachelt@somewhere.com" }
        ]);
    })
    .then(() => {
        console.log("Records inserted successfully");

        // Find all documents in employees collection after insertMany
        return Employee.find();
    })
    .then((data) => {
        console.log("\nDocuments in employees collection after insertMany:");
        console.log(data);
    })
    .catch((error) => {
        console.error("Error:", error);
    })
    .finally(() => {
        mongoose.connection.close(); // Close the MongoDB connection
    });
```

## app_insertOne.js ##

```
const mongoose = require('mongoose');
const Schema = mongoose.Schema;

const Employee = require('./employee');

const uri =  "mongodb://root:MjI4MjMtamthZXdw@localhost:27017";

mongoose.connect(uri,{'dbName':'employeeDB'});

//insertOne record into employee
let newEmployee = new Employee({
    emp_name: 'John Doe',
    age: 37,
    location: "Illinois",
    email: "jdoe@somewhere.com"
});
newEmployee.save().then(function(){
    Employee.find().then((data)=>{
        console.log("\n\nDocuments in employees collection after insertOne")
        console.log(data);
        mongoose.connection.close();
    })
}).catch(function(error){
    console.log(error)
});
```

## app_list.js ##

```
const mongoose = require('mongoose');
const Employee = require('./employee');

const uri =  "mongodb://root:MjI4MjMtamthZXdw@localhost:27017";

mongoose.connect(uri,{'dbName':'employeeDB'});

Employee.find().then((data)=>{
            console.log(data);
            mongoose.connection.close()
        })
```

## app_update.js ##

```
const mongoose = require('mongoose');
const Schema = mongoose.Schema;

const Employee = require('./employee');

const uri =  "mongodb://root:MjI4MjMtamthZXdw@localhost:27017";

mongoose.connect(uri,{'dbName':'employeeDB'})
    .then(() => {
        console.log("Connected to MongoDB");

        // Update one record in employee
        return Employee.updateOne({ emp_name: "John Doe" },
            { email: "jdoe@somewhere.com" });
    })
    .then((updateOneResult) => {
        console.log("Updated Docs for updateOne:", updateOneResult);
        console.log("One record updated");

        // Update many records in employees
        return Employee.updateMany({ age: { $gt: 30 } },
            { location: "New York" });
    })
    .then((updateManyResult) => {
        console.log("Updated Docs for updateMany:", updateManyResult);
        console.log("Many records updated");

    })
    .catch((error) => {
        console.error("Error:", error);
    })
    .finally(() => {
        mongoose.connection.close(); // Close the MongoDB connection
    });
```

## employee.js ##

```
const mongoose = require('mongoose');

const Schema = mongoose.Schema;

const employees = new Schema({
  emp_name: {
    type: String,
    required: true
  },
  age: {
    type: Number,
    required: true,
  },
  location: {
    type: String,
    required: true
  },
  email: {
    type: String,
    required: true
  }
});

module.exports = mongoose.model('employees', employees);
```
