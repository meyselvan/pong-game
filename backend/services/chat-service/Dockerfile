FROM node:latest

WORKDIR /app

COPY package.json ./
COPY package-lock.json ./

RUN npm install

COPY ../../src/modules/chat .

CMD ["npm", "run", "dev"]