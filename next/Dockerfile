FROM node:lts-alpine
WORKDIR /opt/node/next
COPY . .
RUN yarn --production --frozen-lockfile && yarn build

CMD ["yarn","start"]

