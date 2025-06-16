FROM node:20-alpine

ENV PORT=3000
WORKDIR /app

COPY package*.json ./
CMD ["pip install --upgrade pip"]
RUN npm install

COPY . .

EXPOSE 3000
CMD ["npm", "start"]
