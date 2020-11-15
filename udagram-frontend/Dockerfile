# Use node base image
FROM node:13

# Create app directory in Docker
WORKDIR /usr/src/app

# Install app dependencies by copying 
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies  in Docker
npm install

# Install ionic framework's command line tools
npm install -g ionic

# Prepare your application by compiling them into static files 
ionic build

# Copy app from local environment
COPY . .

# Set the application's port number
EXPOSE 8100

# Define Docker's behavior when the image is run
CMD["ionic serve"]


