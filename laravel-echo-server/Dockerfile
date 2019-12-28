FROM node:8.17.0-stretch

ARG APP_DIR=node_app
RUN mkdir -p ${APP_DIR}
WORKDIR ${APP_DIR}

# Installing dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
	nano

COPY ./laravel-echo-server.json /${APP_DIR}/laravel-echo-server.json

RUN npm install -g laravel-echo-server

EXPOSE 3000