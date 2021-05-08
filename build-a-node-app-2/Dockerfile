FROM node:12-stretch

USER node

WORKDIR /home/node/src

COPY --chown=node:node . .

RUN ["yarn", "install"]

EXPOSE 3000

CMD ["node", "index.js"]
