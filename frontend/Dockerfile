# base image
FROM node:12.2.0-alpine

# set working directory
WORKDIR /portfolio

# install and cache app dependencies
COPY package.json ./package.json
RUN npm install
RUN npm install @vue/cli

# start app
CMD ["npm", "run", "serve"]