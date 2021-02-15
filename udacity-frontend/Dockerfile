
# Use NodeJS base image
FROM node:13

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install -g @ionic/cli
RUN npm install

# Copy app source
COPY . .

EXPOSE 8100

# Serve
CMD ["/usr/local/bin/ionic", "serve", "-p", "8100", "--external"]