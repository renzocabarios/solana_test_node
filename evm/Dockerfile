FROM node:20.11.1-alpine

WORKDIR /app

COPY yarn.lock package.json ./

RUN yarn --pure-lockfile

COPY . .

EXPOSE 8545

CMD ["yarn", "hardhat", "node"]
