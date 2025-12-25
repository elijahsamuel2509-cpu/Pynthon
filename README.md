# Pynthon
# Dockerfile for a Node.js cypherx bot FROM node:20-alpine WORKDIR /app  # Install dependencies COPY package*.json ./ RUN npm ci --only=production  # Copy source COPY . .  ENV NODE_ENV=production # Use the port your bot or webhook server listens on EXPOSE 3000  # Use your start script (adjust if different) CMD ["npm", "start"]
