# Full stack application with React , Loopback and MongoDB


1. Clone this repo and navigate to the folder generated, open command line and run
```sh
npm install
 ```
2.  Run the local server
```sh
 node .
 ```
 3. Visit http://localhost:3000 in browser to see the project


## How to start this project from scratch

1. install loopback globally ``` npm i -g loopback-cli  ```
2. Create a project by running the command ```lb ```
3. Select api-server
4. Install mongodb community server in your local machine
5.  install loopback mongodb connector ```npm install loopback-connector-mongodb```
6. connect the datasource to mongodb
``` lb datasource mongoDS --connector mongoDB```
7. this command will ask few questions regarding the setup of app, mostly the port, host, db name etc
8. After this go to datasources.json in the project folder 
9. create a model using the command ``` lb model ```
10. expose to REST API -> give yes
11. common/server -> common
10.give the property names , type and default value
12.  escape out of it by pressing esc key
13. Now that our modal is setup, we can easily do CRUD ops
14. Go to localhost:3000/explorer/
15. We will get a list of all the endpoints available
16. Set up a react project in a separate folder, it can be client_src folder
17. We build our react app and develop it in a different port, finally when the app is done, build it and copy the contents of build folder to 'client' folder of our project 
18. Now in the server/boot/root.js file edit the router.get to simply router.get('/')
19. Finally in the server/middleware.json file replace the files property to this 
``` "files": {

"loopback#static": {

"params": "$!../client"

} 

```

20. Now our application is ready and we can run the app by running ``` node . ``` and goto port 3000 in your browser, you can see your app