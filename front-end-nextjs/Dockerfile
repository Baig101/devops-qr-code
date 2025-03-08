# Use an official Node.js runtime as a parent image
FROM node:18-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json (if available)
COPY package*.json ./

# Install the dependencies (both dependencies and devDependencies)
RUN npm install --production=false

# Copy the rest of the application files to the container
COPY . .

# Build the Next.js application
RUN npm run build

# Expose the port the app will run on
EXPOSE 3000

# Start the Next.js app in production mode
CMD ["npm", "run", "start"]
