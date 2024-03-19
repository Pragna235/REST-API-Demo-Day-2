# REST-API-Demo

## Playbook
* Open VSCode Terminal
*     npm init
* Create a `server.js` file since, `"main": "server.js",` this is the name in main field in this  `package.json`

* `[Note]` : `http is a stateless protocol because it does not store any information regarding its previous requests`

*     npm install express
* Write below code in the `server.js` file and check if the server is running or not
*     //create express app (http server inside) --> Express Module --> Non-core module
      const exp = require('express');                                              //node module --> direct name instead of path
      const app = exp();                                                          //http server is created

      //assign port number
      const port = 4000;
      app.listen(port,()=>console.log(`http server listening in ${port}`));
* To start the server : 
*     node server.js
* Click `ctrl+c` to stop the running server
* Paste the below in your browser to check the response
*     http://localhost:4000/
* `[Note]` : `Client makes the request, API handles the request, Server responds to the request`
* `API is a part of the server - so handling and responding go in the same file`

* Install the `REST Client` extension in VSCode --> (alternative to POSTMAN)
* Right now, we don't use a `REACT APP` so create a `.http` extension file, say `client.http`
* Write all the paths in this file for the `CRUD Operations`
* `[Note]` : `Syntax : api.HTTP_REQUEST(route, req handler)`
* `[Note]` : `Express directly converts JS Object to JSON Object`
* `[Note]` : `Also, ### is a separator that separates the CRUD Operations in the client.http file`
* `[Note]`: `Click on the Send Request button that is generated in the client.http file above the separators to check if the Operation had been successful or not`
* API Routes in the `server.js` for reference :
*     //route to get users
      app.get('/users',(req,res)=>{
          //resend response
          res.send({message:"all users"});
      })

      //route to create user
      app.post('/user',(req,res)=>{
          res.send({message:"User Created"});
      })

      //route to update user
      app.put('/user',(req,res)=>{
          res.send({message:"User Updated"});
      })

      //route to delete user
      app.delete('/user',(req,res)=>{
          res.send({message:"User Removed"});
      })
* To start the server is `watch mode`
*     node --watch server.js
* This is used to restart the server automatically when a change is made instead of doing it manually
