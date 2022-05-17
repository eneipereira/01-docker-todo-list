FROM node:14-alpine as builder
WORKDIR /app
ENV REACT_APP_API_HOST="todoback"
ENV REACT_APP_API_PORT="3001"
ADD node_modules.tar.gz .
COPY . .
RUN npm install && npm run build
EXPOSE 3000
ENTRYPOINT [ "npm", "start" ]