# A Docker Micro Service demonstation.
This involves all a well simple designed system that uses the basic fundamental of docker containerisation with the below 
- Docker Networks
- Container Orcharstration
- Docker Compose
- Debugging Container
- intergration and testing

 # Docker Networks
 Helps in managing communication between the containers, host machine and external network

 # Container Orcharstration 
 This is the automation of the operational tasks required to run containerized services and workloads

 # Docker Compose
 Allows one to define and manage multi-container application using a single YAML file (Container Orcharstration)

 #  Debugging Container
 Will give you the skills to debug code

 # intergration and testing
 Will be able to integrate with others os and do testing

 The main application will contain the below
- Frontend - web application
- Backend - Interaction between DB and frontend
- DB - Where data is stored.

For one to run this docker, simply type docker-compose up at the command prompt which will in turn create the MongoDB from stock mongo inage, backend api which use nodejs ith express built from node:alpine, and finaly the front-end which uses reachjs and built from node:alpine image

# Requirements
Make sure that you have the following installed:
- [node](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-18-04) 
- npm 
- [MongoDB](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/) and start the mongodb service with `sudo service mongod start`

## Navigate to the Client Folder 
 `cd client`

## Run the folllowing command to install the dependencies 
 `npm install`

## Run the folllowing to start the app
 `npm start`

## Open a new terminal and run the same commands in the backend folder
 `cd ../backend`

 `npm install`

 `npm start`

 ### Go ahead and add a product (note that the price field only takes a numeric input)

 ## Debugging 
 ## Install npm install --save source-map-explorer
 ##  Add "analyze": "source-map-explorer 'build/static/js/*.js'"  on package.json on the debug
   ##  `npm run build`
   ##  `npm run analyze`

## When running npm start on ./backend make sure mongodb service is up
![Screenshot from 2024-05-09 08-35-14](https://github.com/mwaskagi/yolo/assets/53992099/e749826c-85b1-49d6-9d1c-dbf669b0f687)


## After building images from the docker file push them to docker hub
![Screenshot from 2024-05-09 08-39-22](https://github.com/mwaskagi/yolo/assets/53992099/3ee532b0-5fc4-4923-8509-c1156535bbcb)
![Screenshot from 2024-05-09 08-39-22](https://github.com/mwaskagi/yolo/assets/53992099/0766c50a-b8d7-406a-b172-708637ddc7d4)






