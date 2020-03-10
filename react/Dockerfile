# build
FROM node:lts-alpine as builder

ENV NODE_ENV production

COPY package*.json /opt/node/react/

WORKDIR /opt/node/react
COPY . /opt/node/react

RUN yarn --production --frozen-lockfile && yarn build

# deploy

FROM nginx:alpine

COPY nginx.conf /etc/nginx/conf.d/default.conf

COPY --from=builder /opt/node/react/build /app/react