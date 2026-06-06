FROM node:20-alpine

USER root
RUN apk add --no-cache git python3 make g++

WORKDIR /usr/src/flowise

COPY --chown=node:node . .

USER node

RUN yarn install
RUN yarn build

ENV PORT=3000
EXPOSE 3000

CMD ["npx", "flowise", "start"]
