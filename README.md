# A Docker demonstation of Orchestration of a 3 layered containerised architecture.
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

## After building images from the docker file push them to docker hub

![Screenshot from 2024-05-05 23-10-18](https://github.com/mwaskagi/yolo/assets/53992099/332a016a-654b-4dea-940d-540a0222a810)




