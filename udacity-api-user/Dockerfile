# Use Node base image
FROM node:13

# Create app directory in docker
WORKDIR /usr/src/app

# Install app dependencies by copying 
# package.json and package.lock.json
COPY package*.json ./

# Install dependencies in docker
Run npm install

# Copy app from local environment into docker image
COPY . .

# Set the API's port number
EXPOSE 8080

# Define Docker's behavior when the image is run
CMD["npm run dev"]