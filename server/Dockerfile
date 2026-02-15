# Node.js resmi imajını kullan (Versiyon 24)
FROM public.ecr.aws/docker/library/node:18

WORKDIR /app

# Paketleri yükle
COPY package*.json ./
# Sadece production paketlerini yükle (daha hafif olur)
RUN npm install --only=production

# Kaynak kodları kopyala
COPY . .

EXPOSE 3000

# Uygulamayı başlat
CMD ["node", "index.js"] 