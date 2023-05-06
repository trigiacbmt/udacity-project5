# Use an official Node.js runtime as a parent image
FROM node:14-alpine

# Set the working directory to /app
WORKDIR /app

# Install dependencies
RUN npm install

# Copy the rest of the application to the working directory
COPY . .

# Build the app for production
RUN npm run build

# Serve the app with a production-ready web server
RUN npm install -g serve
CMD ["serve", "-s", "build", "-l", "3000"]