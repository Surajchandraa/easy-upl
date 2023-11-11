# easy-upl:
make file upload easy. upload in few steps

## Installation:
- `npm i easy-upl`

## Usage:
- ```js
    const express = require('express');
    const app = express();
    const store = require('easy-upl');

    const middleware = store("joshi", null, "send");

    app.post('/uploads', middleware, (req, res) => {
    console.log(req.files);
    res.send("File uploaded successfully!");
    });

    app.listen(5000);


## How to use:
1. Install the module:
    `npm i easy-upl`

2. In your Node.js application:
- Import the required modules:
    ```js
        const express = require('express');
        const app = express();
        const store = require('easy-upl');
    

- Set up the middleware for file uploads:
    ```js
        const middleware = store("directory_name", number_of_files, "field");

- Handle file uploads in your route:
    ```js
        app.post('/uploads', middleware, (req, res) => {
        console.log(req.files);
        res.send("File uploaded successfully!");
        });

## Parameters:
- directory name: The name of the directory where files will be uploaded. The directory must exist in your project's root. (Type: string)

- number of files: The number of files you want to upload. Set to null if the number is not fixed. (Type: number)

- fieldname: The field name used in your request (from Postman or a similar tool). (Type: string)

    
