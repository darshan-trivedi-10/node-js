## Create API using express
- CRUD stands for "Create, Read, Update, and Delete". These are the four basic operations that are typically performed on data in a database or other persistent storage system.
    - "Create" refers to the process of adding new data to the system.
    - "Read" refers to the process of retrieving existing data from the system.
    - "Update" refers to the process of modifying existing data in the system.
    - "Delete" refers to the process of removing data from the system.
- These operations are often exposed through a RESTful API, which allows external clients to interact with the data stored in the system using standard HTTP methods such as GET, POST, PUT, and DELETE.

### Project SetUp
- To initialize the project with npm, you can use the `npm init` command. This will create a `package.json` file in your project directory, which will contain information about your project and its dependencies.
- To install Express in your project, you can use the `npm install express` command and also install body-parser using this command `npm install body-parser`.
- Now create a `index.js` file and copy below code in that file.
- Now run the command  `node index.js` and your server will start.

### Creating API using Express
```js
const express = require('express');
const bodyParser = require('body-parser');
const app = express();

const PORT = 3000;

app.use(bodyParser.urlencoded({ extended: true }));
app.use(bodyParser.json());

var blogsList = [];

app.get('/blogs', (req, res) => {
    return res.status(200).json({
        data: blogsList,
        "success": true
    })
})

app.post('/blogs', (req, res) => {
    let blog_data = req.body;
    blogsList.push(blog_data);
    return res.status(201).json({
        success: true
    })
})

app.listen(PORT, () => {
    console.log("Server started on PORT ", PORT);
})
```
# Simple Blog API

This is a simple blog api which accepts two types of requests:
- GET request to '/blogs' endpoint, which returns a JSON object containing all the blogs.
- POST request to '/blogs' endpoint, which accepts JSON object in request body and stores it in the database.

## Endpoints
- `GET /blogs` : Returns all blogs
- `POST /blogs` : Accepts a JSON object in request body and stores it in the database.
