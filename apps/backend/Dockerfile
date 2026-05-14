FROM node:22-alpine

WORKDIR /app

COPY package.json package-lock.json* .npmrc* ./

RUN npm install --legacy-peer-deps

COPY . .

EXPOSE 9000

CMD ["sh", "-c", "npx medusa db:migrate && npm run start"]