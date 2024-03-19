# REST-API-Demo

## Playbook
* Open VSCode Terminal
*     npm init
* Create a `server.js` file since, `"main": "server.js",` this is the name in main field in this  `package.json`

`[Note]` : `http is a stateless protocol because it does not store any information regarding its previous requests`

*     npm install express
* Write below code in the `server.js` file and check if the server is running or not
*     //create express app (http server inside) --> Express Module --> Non-core module
      const exp = require('express');                                              //node module --> direct name instead of path
      const app = exp();                                                          //http server is created

      //assign port number
      app.listen(4000,()=>console.log("Server is Running"));
*     node server.js
* Click `ctrl+c` to stop the running server
