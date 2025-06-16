FROM node:20-alpine

ENV PORT=3000
WORKDIR /app

COPY result/package*.json ./
RUN npm ci --omit=dev

COPY result/ .

EXPOSE 3000
CMD ["npm", "start"]
