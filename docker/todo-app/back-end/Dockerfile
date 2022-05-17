FROM node:14-alpine as builder
WORKDIR /app
ADD node_modules.tar.gz .
COPY . .
RUN npm install
EXPOSE 3001
ENTRYPOINT [ "npm", "start" ]