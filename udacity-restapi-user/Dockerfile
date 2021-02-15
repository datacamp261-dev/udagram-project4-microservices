# Use NodeJS base image
FROM node:13

# Create app directory
WORKDIR /usr/src/app
# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm ci

# Copy app source
COPY . .

# Bind the port that the image will run on
EXPOSE 8080

# Environment variables
ENV POSTGRES_HOST=udacityudagramphdev2.clyvb8goopmh.eu-central-1.rds.amazonaws.com
ENV POSTGRES_DATABASE=postgres
ENV POSTGRES_PASSWORD=hammond3
ENV POSTGRES_USERNAME=postgres
ENV URL=http://localhost:8100

# Define the Docker image's behavior at runtime
CMD ["npm", "run", "dev"]
