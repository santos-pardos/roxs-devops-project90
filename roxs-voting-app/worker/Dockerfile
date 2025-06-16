FROM node:20-alpine

WORKDIR /app

# Instalar dependencias
COPY worker/package*.json ./
RUN npm ci --omit=dev

# Copiar código
COPY worker/ .

# El worker no expone puertos
CMD ["node", "worker.js"]
