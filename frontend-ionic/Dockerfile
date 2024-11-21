# Use Node.js base image
FROM node:18

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package.json package-lock.json ./

# Install dependencies (including Ionic CLI)
RUN npm install -g @ionic/cli  # Install Ionic CLI globally
RUN npm install  # Install project dependencies

# Copy the rest of the Ionic Angular app code
COPY . .

# Expose the Ionic dev server port
EXPOSE 8100

# Start the Ionic Angular app
CMD ["npm", "run", "ionic:serve"]
