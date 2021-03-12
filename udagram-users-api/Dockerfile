FROM node:13
# Create app directory
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies in Docker
RUN npm ci 

# Copy app from local environment into the Docker image
COPY . .
EXPOSE 8080
CMD [ "npm", "run", "prod" ]