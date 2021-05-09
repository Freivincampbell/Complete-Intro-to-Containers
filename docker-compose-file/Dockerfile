FROM node:12-stretch

RUN yarn global add nodemon

USER node

WORKDIR /home/node/src

COPY --chown=node:node . .

RUN ["yarn", "install"]

EXPOSE 3000

CMD ["nodemon", "index.js"]
