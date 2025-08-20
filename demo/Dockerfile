FROM node:20-alpine
WORKDIR /app

# Install deps using cached layer
COPY package.json package-lock.json* yarn.lock* pnpm-lock.yaml* ./
RUN npm ci || npm install

# App source
COPY . .

EXPOSE 3000
CMD ["npm", "start"]
