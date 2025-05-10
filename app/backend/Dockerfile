FROM node:18

WORKDIR /app/backend

COPY app/backend/package*.json ./
RUN npm install

COPY app/backend/ ./

EXPOSE 5000
CMD ["node", "server.js"]
