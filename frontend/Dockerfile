FROM node:20.11.1-alpine3.18 as builder

WORKDIR /app

COPY package*.json ./
ARG NEXT_PUBLIC_API_URL

ENV NEXT_PUBLIC_API_URL ${NEXT_PUBLIC_API_URL}

RUN npm install 

COPY . .

RUN npm run build

CMD [ "npm","start" ]
