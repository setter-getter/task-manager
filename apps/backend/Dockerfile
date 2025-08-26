# apps/backend/Dockerfile
FROM node:18-alpine

WORKDIR /app

# Копируем package.json
RUN apk update && apk add --no-cache openssl
COPY package*.json ./
COPY prisma ./prisma/

# Устанавливаем зависимости
RUN npm install

# Копируем исходный код
COPY . .

# Генерируем Prisma клиент
RUN npx prisma generate

EXPOSE 4000

# Команда запуска будет переопределена в docker-compose
CMD ["npm", "run", "start"]
