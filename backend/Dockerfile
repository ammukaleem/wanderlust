FROM node:21 AS backend_base

WORKDIR /app

COPY . .

RUN npm i


FROM node:21-slim

WORKDIR /app

COPY --from=backend_base /app .

COPY .env.sample .env

EXPOSE 5000

CMD ["npm", "start"]


