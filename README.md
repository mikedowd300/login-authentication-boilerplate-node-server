# login-authentication-boilerplate-node-server

## Boilerplate code for creating a User Database with MongoDB along with instruction for customization

### For the purposes of understanding the code well enough to customize it as well as to produce your own server from scratch, links to each npm used in this project along with explanations of how they are used will be included in this README.

### Also included in this README you will find:
- Instructions on how to set up a Mongo database in a *dev* environment
- Instructions on how to set up a Mongo database in a *Production* environment
- Instructions to deploy a this server to [Heroku](https://www.heroku.com/)

#### This application was made on a MAC using Node 13.2.0, Atom, iTerm2 for a terminal and Postman.
- Instructions below will assist in this setup of the important parts of this configuration.
- Use any editor and cli you are comfortable with
- The important parts are: Node and Postman

## Installing Node.js
- Go to [Node.js](https://www.nodejs.org/)
- Download the Version of Node with *Latest Features*
- Accept the defaults and you should be good
- In a terminal type ```node -v``` to test your installation
- If v13.2.0 or vAnything then you have installed node correctly

# Installing Postman
- Go to [Postman](https://www.getpostman.com/) download it and follow setup instructions.
- FYI: It may seem you need to sign up, but **you do not** although you may for free.
- Using Postman will be explained as needed

# Installing MongoDB in the *Dev* environment
- Following are instructions to set up MongoDB *locally*. Later there will be instructions to run
MongoDB in a *production* environment, but until the application is tested locally, don't bother
setting it up in *production*.
- The following instructions work for setting up MongoDB on a Mac or Linux machine **only**.
- Go to www.mongodb.com
- There are 3 options:
  * Cloud
  * Server
  * Tools
- Select server
- There you will see 2 more options:
  * MongoDB Community Server
  * MongoDB Enterprise server
- Select the *Community* option, its free
- Before clicking the ``` Download``` button, there are 3 settings you need to set:
  * Version - set this to the Latest
  * Operating System - ```macOS 64-bit x64``` or ```Linux```
  * Package - Choose ```TGZ```
- Press Download and wait
- In the finder, navigate to the *Downloads* directory and find the mongo file you downloaded
- Double click it to extract the contents
- The contents are what is needed to run the MongoDB server.
- Rename the unzipped folder to something more practical like *MongoDB*
- Move the folder inside your User folder
- FYI: *Mongo suggests moving this file into a "data" folder inside the "Root" folder, these
directions diverge from that suggestion*
- Inside of your new folder, make another folder called *mongodb-data*. This is where your data bases
will live.
- From your CLI, from your "User" directory, run the following command: ```pwd```. This will return something like ```/Users/YourName```. Copy this to your clipboard.
- Again from the CLI, run the command (you may paste the first from your clipboard): ```/Users/YourName/mongodb/bin/mongod --dbpath=/Users/YourName/mongodb-data```
- This will start your mongoDB server on port 27017.

# Installing **ROBO 3T**, a GUI Admin tool for MongoDB.
- This tool is part of MongoDB and is not required for MongoDB to function properly, however it is highly suggested that this tool be used as it makes managing your data very simple.
- This tool is for the *Dev* environment **only**.
- Go to [Robo 3T](https://robomongo.org/)
- There are 2 product offerings
  * **Studio 3T**
  * **Robo 3T**
- Select **Robo 3T** this is the free tool good for all operating systems
- Click ```Download Robo 3T```
- On the next page you may need to click ```Download Robo 3T``` again
- Click you operating system from the tab and then select the download button
- Wait while Robo 3T downloads
- Once you open up the File, you should be presented with a tool to drag Robo 3T to the Applications
folder where it belongs.
- In the Applications folder open up Robo 3T, you may then be presented with a security check warning that you have are opening a package from the internet, click ```open```.
- This should open Robo 3T, now you need to create a connection so that Robo 3T knows which database
it is managing.Click ```Connect```
- There are many configurable options, but the only one relevant is the ```Name:``` option. You can
enter anything for a name, a sensible name would be "Local MongoDB Database". Click ```Save```.
- Double click the ```Connect``` button and as long as there is no error message, you are connected.
- For the moment, there are no databases to look at, so to check the connection, on the file menu on
the left, right click the connection you made (it should have the name you entered), a dropdown menu
appears, select **open shell**.
- In the shell provided, enter ```db.version()```.
- This should return a version back and you are good to go.

## NPMs used in this project:
- [express](https://www.npmjs.com/package/express)
- [mongodb](https://www.npmjs.com/package/mongodb) - allows us to interact with our Mongo database from Node. 
