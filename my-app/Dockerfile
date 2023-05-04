FROM node:13.8.0-stretch AS build
WORKDIR /
# COPY package.json ./
COPY . .

RUN npm install
RUN npm run build
RUN ls -la

FROM nginx:latest
COPY nginx.conf /etc/nginx/nginx.conf
COPY index.html /usr/share/nginx/html/index.html