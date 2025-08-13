# Use the official Node.js image as the base image
FROM node:20-slim AS development

# Set the working directory inside the container
WORKDIR /react-project

# Copy package.json and package-lock.json (if exists) to install dependencies
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all other project files
COPY . .

# Expose port for development server (Vite uses 5173 by default)
EXPOSE 5173

# Start the React development server with hot-reloading
CMD ["npm", "run", "dev"]
