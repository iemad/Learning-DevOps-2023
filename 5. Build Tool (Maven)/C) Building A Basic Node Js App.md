
1) Update the Ubuntu VM
2) Install: node, npm
3) Make a directory: `mkdir nodejs-web' and `cd` into it.
4) Command: `npm init` and proceed ahead.
5) ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/2b065dfd-61ed-4602-86da-bacbf149e003)
6) `ls`, a file named `package.json` is created.
7) Install Express: `npm install express`; now `node_modules` folder and `package-lock.json` is created.
8) Create a file like this: `vi app.js` and include the following things:
```// app.js
const express = require('express');
const app = express();
const PORT = 3000; // You can change this to any port you prefer

// Define routes
app.get('/', (req, res) => {
  res.send('Hello, this is the homepage!');
});

app.get('/about', (req, res) => {
  res.send('This is the about page.');
});

app.get('/contact', (req, res) => {
  res.send('Contact us at contact@example.com.');
});

// Start the server
app.listen(PORT, () => {
  console.log(`Server is running on port ${PORT}`);
});
```
8) Start the app: `node app.js`
9) Check it in the browser: `ip_address:3000`


**Unfinished. To be continued**
