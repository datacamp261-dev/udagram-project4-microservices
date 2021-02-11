# Set the base image
FROM node:13

# Create app directory
WORKDIR /usr/src/app

# Copy package.json AND package-lock.json
COPY package*.json ./

# Install all dependencies
RUN npm ci

# Copy the rest of the code
COPY . .

# Expose the port 
EXPOSE 8080

# Environment variables
ENV POSTGRES_HOST=udacityudagramphdev2.clyvb8goopmh.eu-central-1.rds.amazonaws.com
ENV POSTGRES_DATABASE=postgres
ENV POSTGRES_PASSWORD=hammond3
ENV POSTGRES_USERNAME=postgres
ENV URL=http://localhost:8100

# Define the command that should be executed
CMD [ "npm", "run", "dev" ]