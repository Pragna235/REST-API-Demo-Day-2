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
      const port = 4000;
      app.listen(port,()=>console.log(`http server listening in ${port}`));
*     node server.js
* Click `ctrl+c` to stop the running server
* Paste the below in your browser to check the response
*     http://localhost:4000/
`[Note]` : `Client makes the request, API handles the request, Server responds to the request`
`API is a part of the server - so handling and responding go in the same file`

* Install the `REST Client` extension in VSCode --> (alternative to POSTMAN)
* Right now, we don't use a `REACT APP` so create a `.http` extension file, say `client.http`
* Write all the paths in this file for the `CRUD Operations`
