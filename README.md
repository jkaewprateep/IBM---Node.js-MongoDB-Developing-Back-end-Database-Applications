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

## Development IDE or using Notepad ++ application ##

🧸💬 Sample of development IDE for multi-languages development platform, debugging code and communication debugging with published tools and team project.</br>
🐑💬 ➰ Is notepad still alive⁉️ </br>
🥺💬 Still here but this time very busy because of too many non-business activities somebody is trying to create.</br>

[Similarity and differentiation of JavaScript and Node.js with Django on node.js]( https://github.com/jkaewprateep/javascripts_vs_node-js/blob/main/README.md ) </br>
[IBM-Data-Warehousing-Capstone-Project]( https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/README.md ) </br>

<p align="center" width="100%">
    <img width="40%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/DekDee_Client.png">
    <img width="40%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/application_withdatabase.png"> </br>
    <b> My simple client, embedded message for CTI communications | </b>
    <b> My simple client with database communication on web application engine support RedHat and Debian </b> </br>
</p>

---

<p align="center" width="100%">
    <img width="60%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/Screenshot%202024-09-04%20143355.png"> </br>
    <b> Pictures from the Internet </b> </br>
</p>

🧸💬 The backend development is the data communication process and organization control for the solution designed for registration central. </br>
🐑💬 ➰ Working with fast communication updates and responses is desired by many of software solution developers when data application flow and application requirements are crafted, developed, and organized here. </br>

## Data Model ## 

### employee.js ###

🧸💬 Define employee data model .</br>
🐑💬 ➰ A good data model should have infomration required for the process with less time access involved into many sources, multiple-access times are possible but connecting to multiple data sources creates of infomration requirements and infomration updates may required for interactions between the data sources. </br>

[Similarity and differentiation of JavaScript and Node.js with Django on node.js]( https://github.com/jkaewprateep/javascripts_vs_node-js/blob/main/README.md ) </br>

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

### customer.js ###

🧸💬 Define customer data model .</br>

```
// Importing the 'mongoose' library, which is an ODM (Object Data Modeling) library for MongoDB.
const mongoose = require('mongoose');

// Creating a schema using the 'Schema' class from mongoose.
const Schema = mongoose.Schema;

// Defining a schema for the 'customers' collection in MongoDB.
const customersSchema = new Schema({
    // Field for storing the user's name as a string.
    user_name: {
        type: String,   // Data type is String.
        required: true  // The field is required and must have a value.
    },
    // Field for storing the user's password as a string.
    password: {
        type: String,   // Data type is String.
        required: true  // The field is required and must have a value.
    },
    // Field for storing the user's email address as a string.
    email: {
        type: String,   // Data type is String.
        required: true  // The field is required and must have a value.
    },
    // Field for storing the user's age as a number.
    age: {
        type: Number,   // Data type is Number.
        required: true  // The field is required and must have a value.
    }
});

// Creating a model from the schema. This model will represent the 'customers' collection in MongoDB.
// The first argument is the name of the collection, and the second argument is the schema.
const CustomersModel = mongoose.model('customers', customersSchema);

// Exporting the CustomersModel to be used in other parts of the application.
module.exports = CustomersModel;
```

---

## Sample application and configuration ##

### app.js / app_list.js ###

🧸💬 Import module, define a variable, connect to the database, and query for data with MongoDB.find() .</br>
🐑💬 ➰ From the mongoose model use the data model Employee connects to MongoDB database and executes the standard MongoDB command Employee.find() for promise, write into data console, and close connection to the database.</br>
🧸💬 MongoDB has a database connection pool maximum management but database client operation with code handling is preferred, the data management module is a database methods definition created with the project and library mongoose same as in Python and C# language you can modify standard data module methods for external library use, authentication requirements and create shortcut method the repeating process such as data verification or insert and update data record for multiple data tables or database operation.</br>
🐐💬 It is a shared logical process for multiple database operations, authentication, and information attached because of some organizations may require database connection string, database connection information, version, application name, and identity identify information provided when the database connects and use the database for logging in one-time call function method.</br>

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

### app_delete.js ###

🧸💬 Delete database records by condition and error handling with error message return .</br>
🦭💬 By Employee.deleteOne() function method scope of the filter record condition parameter perform and code handling, apply regex expression parameter for emp_name with the alphabet R leading information and database code connection handling. By regular expression filter, we can create flexible data record selection from single expression and useful when working with import string data field. </br>
[Regular expression]( https://github.com/jkaewprateep/lessonfrom_Applied_Text_Mining_in_Python/blob/main/README.md#-sample-of-input-data ) </br>

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

### app_insertMany.js ###

🧸💬 Define constant, connect MongoDB, insert multiple data records, and error handling with error message return .</br>
🐯💬 There is an insert of multiple method functions and there is no insert one method function, The programmer saves time in managing of this data insert function built by the user's requirements and creating the Culture-INFO. Later we create a data method by adding a function in the data module same as insert_or_update but utilizes the data information result set to return for the same format method for insert many and insert one record.</br>
🦁💬 That is a good thing that MongoDB has a built-in function for insertion and update and the platform programmer utilizes the idea and creates a modified of the data module, returns result set format for one record return, empty, custom error message and information for communications. In the later versions of MongoDB the data return for one record dataset and many record datasets are the same format and you can specify in the filter for information required to add into the results set for application build communication protocol, seems mongoDB understands of these requirements well.</br>

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

### app_insertOne.js ###

🧸💬 Define constant, connect MongoDB, insert one data record, and error handling with error message return .</br>
🐑💬 ➰ In the case of communication limited on the remote database server or versions of driver communication limited the insertOne() is working, the save function is the confirmation result method and the platform programmer selects to use the save function because the effects are confirmed result and _id information insert into the result set.</br>
🦭💬 That is because I do not want to lookup the database for _id filed again that is my programming logic, selecting a good function will return life safely.</br>

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

### app_update.js ###

🧸💬 Define constant, connect MongoDB, update one data record with filter condition, and error handling with error message return .</br>
🐯💬 In MongoDB there are updateOne and updateMany and if you select updateMany function you save time in validating results because you build your own dataset to update and specific record expression conditions where updateOne you may need to summarize, in the data module in any of the method requirements of updateOne or updateMany the platform programmer create summarize function for return result set format and validation of dependent field in one time as Culture-INFO. MongoDB fast builds and works with transactions when performed summarize for data validation and the data aggregate technique can be performed in a scheduled process or instance process with multiple records requested at one time.</br>

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

### employee_list_app.js ###

🧸💬 Define constant, application methods, module export variable, define add_employee .</br>

```
const mongoose = require('mongoose');
const Employees = require('./employee');

const express = require('express');
// Added
const cors = require('cors');

const bodyParser = require('body-parser');

const app = express();
const port = 3002;

//Replace the password in the line below
const uri =  "mongodb://root:MjI4MjMtamthZXdw@localhost:27017";

mongoose.connect(uri,{'dbName':'employeeDB'});

// Enable CORS for all routes
app.use(cors());

// Middleware to parse JSON requests
app.use("*",bodyParser.json());

// GET endpoint
app.get('/api/employees', async (req, res) => {
    const documents = await Employees.find();
    res.json("🧸💬  " + documents);
});

app.post('/api/add_employee', async (req, res) => {
    console.log(req);
    const data = req.body;
    const emp = new Employees({
      "emp_name": data['name'],
      "age": data['age'],
      "location": data['location'],
      "email": data['email']
    });
    // Save the employee to the database
    await emp.save();
    res.json({ message: '🧸💬  Employee added successfully' });
  });

// Start the server
app.listen(port, () => {
  console.log(`Server is running on http://localhost:${port}`);
});
```

### customer_app.js ###

🧸💬 Define constant, application methods, module export variable, define login, and add_customer .</br>

```
// Importing necessary libraries and modules
const mongoose = require('mongoose');            // MongoDB ODM library
const Customers = require('./customer');         // Imported MongoDB model for 'customers'
const express = require('express');              // Express.js web framework
const bodyParser = require('body-parser');       // Middleware for parsing JSON requests
const path = require('path');                    // Node.js path module for working with file and directory paths

// Creating an instance of the Express application
const app = express();

// Setting the port number for the server
const port = 3000;

// MongoDB connection URI and database name
const uri =  "mongodb://root:your_password@localhost:27017";
mongoose.connect(uri, {'dbName': 'customerDB'});

// Middleware to parse JSON requests
app.use("*", bodyParser.json());

// Serving static files from the 'frontend' directory under the '/static' route
app.use('/static', express.static(path.join(".", 'frontend')));

// Middleware to handle URL-encoded form data
app.use(bodyParser.urlencoded({ extended: true }));

// POST endpoint for user login
app.post('/api/login', async (req, res) => {
    const data = req.body;
    console.log(data);
    let user_name = data['user_name'];
    let password = data['password'];

    // Querying the MongoDB 'customers' collection for matching user_name and password
    const documents = await Customers.find({ user_name: user_name, password: password });

    // If a matching user is found, set the session username and serve the home page
    if (documents.length > 0) {
        res.send("User Logged In");
    } else {
        res.send("User Information incorrect");
    }
});

// POST endpoint for adding a new customer
app.post('/api/add_customer', async (req, res) => {
    const data = req.body;
    console.log(data)
    const documents = await Customers.find({ user_name: data['user_name']});
    if (documents.length > 0) {
        res.send("User already exists");
    }
    
    // Creating a new instance of the Customers model with data from the request
    const customer = new Customers({
        "user_name": data['user_name'],
        "age": data['age'],
        "password": data['password'],
        "email": data['email']
    });

    // Saving the new customer to the MongoDB 'customers' collection
    await customer.save();

    res.send("Customer added successfully")
});

// GET endpoint for the root URL, serving the home page
app.get('/', async (req, res) => {
    res.sendFile(path.join(__dirname, 'frontend', 'home.html'));
});

// Starting the server and listening on the specified port
app.listen(port, () => {
    console.log(`Server is running on http://localhost:${port}`);
});
```

---

## Statics resoources management ##

### fileuploadapp.js ###

🧸💬 Define constant, application methods, module export variable, define upload file and directory list .</br>

```
const express = require('express');
const multer = require('multer');
const path = require('path');
const fs = require('fs');

const app = express();
const port = 3000;

// Define the upload directory path
const directoryPath = 'uploads/';

// Set up storage for uploaded files
const storage = multer.diskStorage({
  destination: function (req, file, cb) {
    cb(null, directoryPath); // Specify the upload directory
  },
  filename: function (req, file, cb) {
    cb(null, file.originalname); // Use the original file name
  },
});

const upload = multer({ storage: storage });

// Serve the HTML form for file upload
app.get('/', (req, res) => {
  res.sendFile(path.join(__dirname, 'index.html'));
});

// Handle file upload
app.post('/upload', upload.single('file'), (req, res) => {
  if (!req.file) {
    return next(new Error('No file uploaded.'));
  }

  // Access the uploaded file information
  const uploadedFile = req.file;
  console.log('Uploaded file:', uploadedFile);

  fs.readdir(directoryPath, (err,files)=>{
    if (err) {
      return res.status(500).send('Error reading directory.');
    }
    strfilenames = `<a href='/'>Home</a><br/>

`;

    files.forEach((file)=>{
      strfilenames = `${strfilenames} <a target='_blank' href='file/${file}'>${file}</a><br/>

`;
    });
    res.send(strfilenames)
  });

});

// Serve uploaded files using express.static middleware
app.use('/file', express.static('uploads'));

// Start the server
app.listen(port, () => {
  console.log(`Server is running on http://localhost:${port}`);
});
```

---

## Securely connection and encryption ##

### jwt ###

🧸💬 Define constant, application methods, module export variable, define register, login and dashboard with jwt secured compoent .</br>

```
// index.js

const express = require('express');
const jwt = require('jsonwebtoken');

const app = express();
const secretKey = 'yourSecretKey'; // Replace with your own secret key

app.use(express.json());

// Sample user data (Replace with your database or actual authentication logic)
const users = [];

// Endpoint for user registration
app.post('/register', (req, res) => {
  const { username, password } = req.body;

  // Check if the username already exists
  const existingUser = users.find((u) => u.username === username);
  if (existingUser) {
    return res.status(400).json({ message: 'Username already exists' });
  }

  // Add new user to the database
  const newUser = {
    id: users.length + 1,
    username,
    password,
  };
  users.push(newUser);

  res.status(201).json({ message: 'User registered successfully' });
});

// Endpoint for user login
app.post('/login', (req, res) => {
  const { username, password } = req.body;

  // Find user by username and password
  const user = users.find((u) => u.username === username && u.password === password);

  if (user) {
    // User authenticated, generate token
    const token = jwt.sign({ id: user.id, username: user.username }, secretKey);
    res.json({ token });
  } else {
    res.status(401).json({ message: 'Invalid credentials' });
  }
});

// Protected route example (Dashboard access)
app.get('/dashboard', verifyToken, (req, res) => {
  // Return dashboard data or user-specific information
  res.json({ message: ' 🧸💬  Welcome to the Customer Portal!' });
});

// Middleware to verify token
function verifyToken(req, res, next) {
  const token = req.headers['authorization'];

  if (typeof token !== 'undefined') {
    jwt.verify(token, secretKey, (err, authData) => {
      if (err) {
        res.sendStatus(403);
      } else {
        req.authData = authData;
        next();
      }
    });
  } else {
    res.sendStatus(401);
  }
}

// Start server
const PORT = 3003;
app.listen(PORT, () => {
  console.log(`Server running on port ${PORT}`);
});
```

### customer_app.js ( encryption message ) ###

🧸💬 Define constant, application methods, module export variable, define registration, and login and logout method .</br>

```
// Added
const bcrypt = require("bcrypt")
const session = require('express-session');
const saltRounds = 5
const password = "admin"

// Importing necessary libraries and modules
const mongoose = require('mongoose');            // MongoDB ODM library
const Customers = require('./customer');         // Imported MongoDB model for 'customers'
const express = require('express');              // Express.js web framework
const bodyParser = require('body-parser');       // Middleware for parsing JSON requests
const path = require('path');                    // Node.js path module for working with file and directory paths

// Creating an instance of the Express application
const app = express();

// Added
const uuid = require('uuid'); //to generate a unique session id

app.use(session({
      cookie: { maxAge: 120000 }, // Session expires after 2 minutes of inactivity
    secret: 'itsmysecret',
    res: false,
    saveUninitialized: true,
    genid: () => uuid.v4()
}));

// Setting the port number for the server
const port = 3000;

// MongoDB connection URI and database name
const uri =  "mongodb://root:MjI4MjMtamthZXdw@localhost:27017";
mongoose.connect(uri, {'dbName': 'customerDB'});

// Middleware to parse JSON requests
app.use("*", bodyParser.json());

// Serving static files from the 'frontend' directory under the '/static' route
app.use('/static', express.static(path.join(".", 'frontend')));

// Middleware to handle URL-encoded form data
app.use(bodyParser.urlencoded({ extended: true }));

// POST endpoint for user login
app.post('/api/login', async (req, res) => {
    const data = req.body;
    console.log(data);

    let user_name = data['user_name'];
    let password = data['password'];

    // Querying the MongoDB 'customers' collection for matching user_name and password
    const documents = await Customers.find({ user_name: user_name });

    // If a matching user is found, set the session username and serve the home page
    if (documents.length > 0) {
        let result = await bcrypt.compare(password, documents[0]['password'])
        if(true) {
            const genidValue = req.sessionID;
            res.cookie('username', user_name);
            res.sendFile(path.join(__dirname, 'frontend', 'home.html'));
        } else {
            res.send("Password Incorrect! Try again");
        }
    } else {
        res.send("User Information incorrect");
    }
});

// POST endpoint for adding a new customer
app.post('/api/add_customer', async (req, res) => {
    const data = req.body;

    const documents = await Customers.find({ user_name: data['user_name']});
    if (documents.length > 0) {
        res.send("User already exists");
    }

    let hashedpwd = bcrypt.hashSync(data['password'], saltRounds)

    // Creating a new instance of the Customers model with data from the request
    const customer = new Customers({
        "user_name": data['user_name'],
        "age": data['age'],
        "password": hashedpwd,
        "email": data['email']
    });

    // Saving the new customer to the MongoDB 'customers' collection
    await customer.save();

    res.send("Customer added successfully")
});

// Added
// GET endpoint for user logout
app.get('/api/logout', async (req, res) => {
    req.session.destroy((err) => {
        if (err) {
          console.error(err);
        } else {
          res.cookie('username', '', { expires: new Date(0) });
          res.redirect('/');
        }
      });
});

// GET endpoint for the root URL, serving the home page
app.get('/', async (req, res) => {
    res.sendFile(path.join(__dirname, 'frontend', 'home.html'));
});

// Starting the server and listening on the specified port
app.listen(port, () => {
    console.log(`Server is running on http://localhost:${port}`);
});
```

---

## Sample ##

<p align="center" width="100%">
	<img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web01.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web02.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web03.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web04.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web05.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web06.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web07.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web08.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web09.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web10.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web11.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web12.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web13.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web14.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web15.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web16.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web17.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web18.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web19.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web20.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web21.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web22.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web23.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web24.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web25.png">
    <img width="25%" src="https://github.com/jkaewprateep/IBM---Node.js-MongoDB-Developing-Back-end-Database-Applications/blob/main/web26.png">	</br>
</p>

---

<p align="center" width="100%">
    <img width="30%" src="https://github.com/jkaewprateep/advanced_mysql_topics_notes/blob/main/custom_dataset.png">
    <img width="30%" src="https://github.com/jkaewprateep/advanced_mysql_topics_notes/blob/main/custom_dataset_2.png"> </br>
    <b> 🥺💬 รับจ้างเขียน functions </b> </br>
</p>
