# apps/frontend/Dockerfile
FROM node:18-alpine

WORKDIR /app

# Копируем package.json
COPY package*.json ./

# Устанавливаем зависимости
RUN npm install

# Копируем исходный код
COPY . .

EXPOSE 5173

# Команда запуска будет переопределена в docker-compose
CMD ["npm", "run", "dev"]
