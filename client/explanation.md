# Client and backend
- Base Image : - node:10-slim image due to it size and also has few dependancies making it stable for my project for client while node:alpine  for the backend

# Docker Directive
-  i have used 7 steps 
    FROM : call the base image to be used
    WORKDIR : create an app directory for my application
    COPY : copy the json file to container
    RUN :  Install the dependencies in the container
    COPY : copy the ap
    EXPOSE : declare the port to be used
    CMD : start the app

# Docker Compose Networking
- Port exposed for the client were 3000:3000 and backend 5000:5000 for both app and container, while for the database used the default 27017:27017

# Volume 
- this is useful for storing data outside the container so that even if the container is stopped or deleted one cannot loose the data. Our data is been stored on /var/lib/mongod

# Debugging
- 
