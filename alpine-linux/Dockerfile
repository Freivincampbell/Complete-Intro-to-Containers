FROM node:12-alpine

USER node

RUN mkdir /home/node/code

WORKDIR /home/node/code

COPY --chown=node:node yarn.lock package.json ./

RUN ["yarn", "install"]

COPY --chown=node:node . .

CMD ["node", "index.js"]
