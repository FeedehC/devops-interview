FROM node:12.22.5-alpine3.14
#FROM node:18.2-alpine3.14
#FROM node:carbon
# Create app directory
WORKDIR /app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./
#To bundle your app’s source code inside the Docker image, use the COPY instruction:
COPY . .

RUN npm install

#Your app binds to port 3000 so you’ll use the EXPOSE instruction to have it mapped by the docker daemon:
EXPOSE 3000

CMD [ "npm", "start" ]