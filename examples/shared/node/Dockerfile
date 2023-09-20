FROM node:20.7-bullseye-slim@sha256:f42ad17f8078f87737d19ae7bab45ae02ddd50aa52b6816f6d56c57f000f7b6c as node-base


FROM node-base as node-http-auth
ARG NODE_APP=.
ARG NODE_APP_NAME=http-service/server
# Add an env to save ARG
ENV NODE_APP_PATH "/app/${NODE_APP_NAME}"
COPY "$NODE_APP" /app
# Dont use exec form to interpolate correctly
CMD node $NODE_APP_PATH
