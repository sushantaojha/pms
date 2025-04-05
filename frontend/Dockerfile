FROM node:16 AS build

WORKDIR /app 

COPY package*.json .

RUN npm install

COPY . .

#RUN apk update && apk add --no-cache openssl

RUN npm run build

#RUN npm install -g serve 

# EXPOSE 5000

CMD ["npm", "start"]
