FROM node:21 AS frontend_base

WORKDIR /app

COPY package*.json ./

RUN npm i

COPY . .

FROM node:21-slim

WORKDIR /app1

COPY --from=frontend_base /app .

COPY .env.sample .env.local

EXPOSE 5173

CMD ["npm", "run", "dev", "--", "--host"]

