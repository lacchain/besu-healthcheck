 
FROM node:8.11.1-alpine
RUN apk update && apk upgrade && apk add --no-cache bash git openssh
RUN apk add --update python krb5 krb5-libs gcc make g++ krb5-dev
WORKDIR '/app'
COPY ./package.json ./
RUN npm install
COPY . .
CMD ["node","index.js"]