FROM mjgargani/puppeteer:trybe1.0
WORKDIR /app
ENV FRONT_HOST="todofront"
ENV FRONT_PORT="80"
ADD node_modules.tar.gz ./
COPY . .
ENTRYPOINT [ "npm", "test" ]