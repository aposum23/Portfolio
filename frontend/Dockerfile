FROM node:12.2.0-alpine
WORKDIR /frontend
COPY package.json ./
RUN  npm install
EXPOSE 8080
CMD ["npm", "run", "serve"]