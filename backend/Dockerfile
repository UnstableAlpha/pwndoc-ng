FROM node:22-alpine

RUN mkdir -p /app
WORKDIR /app
COPY package*.json ./
RUN apk --no-cache add --virtual builds-deps build-base python3 git
RUN npm install
COPY . .
EXPOSE 4242
ENV NODE_ENV=prod
ENV NODE_ICU_DATA=node_modules/full-icu
ENTRYPOINT ["npm", "start"]
