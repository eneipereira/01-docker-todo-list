FROM mjgargani/puppeteer:trybe1.0
WORKDIR /app
ENV FRONT_HOST="todofront"
ENV FRONT_PORT="3000"
ADD node_modules.tar.gz ./
COPY . .
ENTRYPOINT [ "npm", "test" ]