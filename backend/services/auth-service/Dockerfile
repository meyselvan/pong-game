FROM node:latest

WORKDIR /app

COPY package.json ./
COPY package-lock.json ./

RUN npm install

COPY ../../src/modules/auth .

CMD ["npm", "run", "dev"]