FROM node:12-stretch

USER node

WORKDIR /home/node/src

COPY --chown=node:node package.json yarn.lock ./

RUN ["yarn", "install"]

EXPOSE 3000

CMD ["node", "index.js"]
