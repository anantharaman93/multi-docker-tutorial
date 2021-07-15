FROM node:alpine
# FROM node:14.14.0-alpine

USER node

RUN mkdir -p /home/node/app
WORKDIR '/home/node/app'

COPY --chown=node:node ./package.json ./
RUN npm install
COPY --chown=node:node ./ ./

CMD ["npm", "run", "start"]

# RAN USING
# docker run -p 3000:3000 -v /home/node/app/node_modules -v $(pwd):/home/node/app <container-id>%