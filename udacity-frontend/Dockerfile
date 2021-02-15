  
## Build
FROM node:13 as build
WORKDIR /app
COPY package*.json /app/
RUN npm ci
COPY ./ /app/ 
RUN npm install -g @ionic/cli
RUN ionic build

## Run 
FROM nginx:alpine
RUN rm -rf /usr/share/nginx/html/*
#COPY www /usr/share/nginx/html
COPY --from=build  /app/www /usr/share/nginx/html