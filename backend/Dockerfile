# Development stage
FROM node:18-alpine AS development

WORKDIR /app

# Copy package files first for better caching
COPY package*.json ./
COPY tsconfig*.json ./

# Install dev dependencies
RUN npm install

# Copy source code
COPY . .

# Build TypeScript
RUN npm run build

# Production stage
FROM node:18-alpine AS production

WORKDIR /app

# Install production dependencies only
COPY package*.json ./
RUN npm install --only=production

# Copy built files from development stage
COPY --from=development /app/dist ./dist
COPY --from=development /app/ormconfig.json .

# Copy wait script and make executable
COPY wait-for-postgres.sh .
RUN chmod +x wait-for-postgres.sh

# Environment variables will be set in compose file
EXPOSE 3000

CMD ["sh", "-c", "./wait-for-postgres.sh && node dist/index.js"]