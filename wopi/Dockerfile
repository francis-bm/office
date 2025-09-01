FROM node:18-alpine

# Create app dir
WORKDIR /usr/src/app

# Copy package files first for caching
COPY package*.json ./

# Install dependencies
RUN npm ci --production

# Copy app
COPY . .

# Expose the port
ENV PORT=5000
EXPOSE ${PORT}

# Run the app (use your actual start script)
CMD ["node", "index.js"]
