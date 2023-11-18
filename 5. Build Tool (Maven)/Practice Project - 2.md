# Building A Basic Node Js App

## Part - 1) A Very Basic Node JS Application Deployment with Maven:
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
10) If we would like to get something like `npm start` to get our application started then we can do something like this:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/738dbc93-31eb-4134-b6dc-3295b44d2d50)
    Instead of that line, we can put: `"test": "node app.js"`, then we can run the application by `npm start`


## Part - 2) A Basic Node JS Application Deployment with Maven:
1) In the same folder, make two new HTML files `index.html` and `about.html` [from here](https://github.com/iemad/Basic_NodeJS_WebApp_Public)
2) Change app.js following the link given in step 1. Now application is listening on port 8081 as stated in the app.js file.


## Part - 3) Run he Application from a Docker Image:
1) Let's try to understand how Docker will play the role here:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/9c89388e-e25f-4536-a0c9-dd322e58e090)

   - FROM node:alpine </br>
     This is the base image
   - COPY ./ ./ </br>
     Copying everything from project folder to the container
   - RUN npm install
     This will get necessary things from package.json file
   - EXPOSE 8081
     8081 will be opened in the container

2) Create a Dockerfile and paste the contents from the above repo.
3) Now get the Docker installed: `sudo apt install docker.ip -y`
4) Make sure that the user 'ubuntu' gets access to Docker commands: `sudo usermod -aG docker ubuntu`
5) Logout and login: `newgrp docker`
6) Build the image: `docker build -t node-webapp:latest .`
7) Check the docker image: `docker images`
8) Run it: `docker run -d --name node-app-from-container -p 8088:8081 node-webapp:latest`
9) Check the container: `docker ps`
10) Check the application now: `IP:8088`
  




























