FROM node:12.16.1

WORKDIR /front

ENV PATH /front/node_modules/.bin:$PATH

COPY package.json /front/package.json

RUN npm install

COPY . /front

RUN npm run build

CMD npm run serve
