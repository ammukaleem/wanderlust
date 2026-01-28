FROM node:21 AS backend_base

WORKDIR /app

COPY . .

RUN npm i


FROM node:21-slim

WORKDIR /app1

COPY --from=backend_base /app .

COPY .env.docker .env

EXPOSE 5000

CMD ["npm", "start"]


