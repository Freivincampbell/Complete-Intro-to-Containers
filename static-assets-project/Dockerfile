FROM node:12-stretch AS builder
WORKDIR /app
COPY . .
RUN  yarn install
RUN  yarn build

FROM nginx:1.17
COPY --from=builder /app/build /usr/share/nginx/html
