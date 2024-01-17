FROM node:21.6-bullseye-slim@sha256:ef46f8bf489e6a6c2d056e0c0bec23a4120b34aabb9551a446baf68282defa01 as node-base


FROM node-base as node-http-auth
ARG NODE_APP=.
ARG NODE_APP_NAME=http-service/server
# Add an env to save ARG
ENV NODE_APP_PATH "/app/${NODE_APP_NAME}"
COPY "$NODE_APP" /app
# Dont use exec form to interpolate correctly
CMD node $NODE_APP_PATH
