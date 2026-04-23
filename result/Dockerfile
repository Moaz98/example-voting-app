# Base Image
FROM node:8.9-alpine

# Set working directory
WORKDIR /app

# Copy package files first (better caching)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy remaining application code
COPY . .

# Expose port
EXPOSE 80

# Run the application
CMD ["node", "server.js"]
