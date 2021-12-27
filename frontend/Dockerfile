FROM node:16-alpine as builder

USER node

RUN mkdir -p /home/node/app
WORKDIR /home/node/app

COPY --chown=node:node ./package.json ./
RUN npm install

# Copy the source code to the app directory
COPY --chown=node:node ./ ./

# Build the app; output in /home/node/app/build
RUN npm run build

FROM nginx
# Copy the builf result from the previous step to the nginx container
COPY --from=builder /home/node/app/build /usr/share/nginx/html