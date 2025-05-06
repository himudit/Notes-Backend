# Notes-Backend

By Default we use Common JS,ejs,cjs

npm init -> creates package.json  
npm i express -> install express  
npm i --save-dev-nodemon  also do "dev" : "nodemon server.js" in package.json and do npm run dev  
npm install dotenv  

// remember No quotes around values, no semicolon  
PORT=5000  
SECRET_KEY=supersecret  



server.js  
const express = require('express');  
const app = express();  
require('dotenv').config();  

const PORT = process.env.PORT || 2000;  

app.use(express.json()); -> the frontend send the data in json-format in req.body so to parse it we need this otherwie the req.body() will be undefined   

app.listen(8000, () => {  
    console.log('server is running on port 8000');  
})  
