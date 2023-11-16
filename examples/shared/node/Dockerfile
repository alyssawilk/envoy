FROM node:21.2-bullseye-slim@sha256:3af44b6a2df08a48d0fc0598f6d714451dca4fb77a65292a402accd51175b738 as node-base


FROM node-base as node-http-auth
ARG NODE_APP=.
ARG NODE_APP_NAME=http-service/server
# Add an env to save ARG
ENV NODE_APP_PATH "/app/${NODE_APP_NAME}"
COPY "$NODE_APP" /app
# Dont use exec form to interpolate correctly
CMD node $NODE_APP_PATH
