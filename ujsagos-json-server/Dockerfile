FROM node:20-alpine3.17

WORKDIR /app

RUN npm i json-server@0.17.4 multer body-parser@1.19.0

RUN mkdir config && mkdir data

COPY config/json-server.json config/json-server.json

COPY data/db.json data/db.json
COPY data/routes.json data/routes.json

COPY public public

EXPOSE 3000
ENTRYPOINT ["npx", "json-server", "data/db.json"]
CMD ["-c", "config/json-server.json", "-r", "data/routes.json", "--watch", "data/db.json"]