FROM node:22-alpine

WORKDIR /app

# Patch OS-level security vulnerabilities in the Alpine base image
RUN apk update && apk upgrade --no-cache

COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]