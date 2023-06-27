FROM node:16-alpine

WORKDIR /var/www/dices/front

COPY .npmrc .
COPY package.json .
COPY yarn.lock .

RUN yarn install

COPY . .

RUN yarn build

CMD ["node", ".output/server/index.mjs"]