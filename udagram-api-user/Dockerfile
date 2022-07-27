# syntax=docker/dockerfile:1

FROM node:12

#deployment environment
#ENV NODE_ENV=production

# Create app directory
WORKDIR /usr/src/app

# A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
COPY package*.json ./

# Install app dependencies
RUN npm ci

# Bundle app source
COPY . .
EXPOSE 8080
CMD [ "npm", "run", "prod" ]
