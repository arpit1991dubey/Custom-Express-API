# Custom-Express-API
A custom Expreess API with MongoDB Atlas via mongoose + nodemon + JWT(creation and usage) + Password hashing in database.
# Dependencies setup  
1- Open the termimal and switch back to the main workspace and create new directory 'mkdir track-server' (mkdir works in windows as well).
2- Move inside the directory and  run 'npm init -y' to genererate a package.json file.
3- Now installing the dependencies for our API run 'npm install bcrypt express jsonwebtoken mongoose nodemon'.  
4- Make a new directory named src and inside that create 'index.js' this will contain your routes to your express API.  
5- In the 'index.js' import your express and app also make a function for reqest and responce and try to send some data using res.send("Message")  
6- Flip back to the terminal and type 'node src/index.js'.  
7- You will have a popup screen like this(Don't worry about the mongo thing right now).
![](Resturant%20search%20demo/resturant%20search.gif)
# Setting Up MongoDB  
8- MongoDB will store all of our user data externall in a external server, we will use a library known as 'mongoose' to integrate our express api with the database.  
9- We'll use a free hosted copy of mongoDB , navigate to www.cloud.mongodb.com to know furter.  
10- Click on Build a cluster in the main screen an then choose anyone between aws,google cloud and asure and try to choose a region near to you (i chose the mumbai region) and then click on create cluster (it shall take 7-8 mins).  
11- Now click on connect button and whitelist your IP adress (you can also make it accesable from anywhere) .  
12- Create a mongoDB user add a username and password, click on 'connect your application' 
13- Copy the connection string to use in the code.  
14- Replace the <password> with your original one.  
15- Go to the package.json section and replace the "script" section with "dev":nodemon src/index.js" so that anytime we make any changes to the server code, it automatically re-loads the server and applies the new configuration.  
16- Now run 'npm run dev' in the termianl.  
17- Use postman to see the requests (here post request).  
18- Go to www.getpostman.com  and downlod postman.  
19- Create the database model (schema) to manipulate the given collection of data.  
20- Now just imagine a thirdparty applicaation 'postman' which is working like your app which is sending and receiving you requests and dispaying them to you, here your express api is just a medium or waiter between the app and the database.  
21- Below is the visual of postman processing a post request to the /signup page, with a json object as input.  
  ![](Resturant%20search%20demo/resturant%20search.gif)  
22- You can go to your cluster section and check the json inputs that we gave through the app (now postman).  
  ![](Resturant%20search%20demo/resturant%20search.gif) 
23- Any duplicate or empty json object will be declined by mongo itself you need not write the code for this purpose.  
24- Create the json web token and wire it with the API.  
25- The middleWare function will check for the authentic token and repond in a positive or negaive way in either case.  
26- 
