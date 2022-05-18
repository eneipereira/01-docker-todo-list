FROM node:14-alpine as builder
WORKDIR /app
ENV REACT_APP_API_HOST="todoback"
ENV REACT_APP_API_PORT="3001"
ADD node_modules.tar.gz .
COPY . .
RUN npm install && npm run build

FROM nginx:1.16.0-alpine AS prod
COPY --from=builder /app/.nginx/nginx.conf /etc/nginx/conf.d/default.conf
WORKDIR /usr/share/nginx/html
RUN rm -rf ./*
COPY --from=builder /app/build .
EXPOSE 80
ENTRYPOINT ["nginx", "-g", "daemon off;"]