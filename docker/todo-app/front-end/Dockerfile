FROM node:14-alpine as builder
WORKDIR /app
ENV API_HOST="todoback" \
    REACT_APP_API_HOST=${API_HOST}
ENV API_PORT="3001" \
    REACT_APP_API_PORT=${API_PORT}
ADD node_modules.tar.gz .
COPY . .
RUN npm install && npm run build
EXPOSE 3000
ENTRYPOINT [ "npm", "start" ]