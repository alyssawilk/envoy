FROM node:21.5-bullseye-slim@sha256:a46d5f82c3c88ff4870bff5203e9fda43699719e3a458a4dbf4691e80951db5a as node-base


FROM node-base as node-http-auth
ARG NODE_APP=.
ARG NODE_APP_NAME=http-service/server
# Add an env to save ARG
ENV NODE_APP_PATH "/app/${NODE_APP_NAME}"
COPY "$NODE_APP" /app
# Dont use exec form to interpolate correctly
CMD node $NODE_APP_PATH
