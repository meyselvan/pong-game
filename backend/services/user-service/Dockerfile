FROM node:latest

WORKDIR /app

COPY ../../package.json ./
COPY ../../package-lock.json ./

RUN npm install

COPY ../../src/modules/user .

CMD ["npm", "run", "dev"]