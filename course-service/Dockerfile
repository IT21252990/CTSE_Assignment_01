# Use Node.js LTS version as the base image
FROM node:20-slim

# Set working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all application files
COPY . .

# Expose the port your application runs on
EXPOSE 5000

# Command to run the application
CMD ["node", "index.js"]