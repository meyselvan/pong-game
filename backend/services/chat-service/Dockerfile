FROM node:18-alpine

WORKDIR /app

# Package files'ı kopyala
COPY ./backend/package*.json ./

# Dependencies'leri yükle
RUN npm ci --only=production

# Backend source code'unu kopyala
COPY ./backend/src ./src
COPY ./backend/.env* ./

# SQLite database klasörünü oluştur
RUN mkdir -p /data

# Port'u expose et
EXPOSE 3000

# Health check ekle
HEALTHCHECK --interval=30s --timeout=3s --start-period=5s --retries=3 \
  CMD node -e "require('http').get('http://localhost:3000/health', (res) => { process.exit(res.statusCode === 200 ? 0 : 1) })"

# Auth service'i başlat
CMD ["node", "src/server.js"]