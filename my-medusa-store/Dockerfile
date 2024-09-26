FROM node:20.17.0

# Set the working directory
WORKDIR /usr/src/app

# Copy package files first
COPY package.json ./
COPY package-lock.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Install Medusa CLI globally
RUN npm install -g @medusajs/medusa-cli

# Expose the port for the Medusa backend
EXPOSE 9000

# Command to start the Medusa backend without running migrations
CMD ["medusa", "develop"]