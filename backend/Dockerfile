# lite image
FROM node:alpine  

# set working directory
WORKDIR /app

# add `/app/node_modules/.bin` to $PATH
ENV PATH /app/node_modules/.bin:$PATH

# install app dependencies
COPY package.json ./
COPY package-lock.json ./
COPY server.js ./
COPY upload.js ./

RUN npm install

# add app
COPY . .

#expose port
EXPOSE 5000
# start app
CMD ["node", "server.js"]