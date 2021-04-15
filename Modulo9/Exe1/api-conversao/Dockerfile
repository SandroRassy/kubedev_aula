FROM node:15.12.0-alpine3.12
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node","index.js"]