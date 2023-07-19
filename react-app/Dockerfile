# Stage 1: Build the application
FROM node:18-alpine AS build

WORKDIR /app

ENV PATH /app/node_modules/.bin:$PATH

COPY package*.json ./

RUN npm install --silent
RUN npm install @mui/material @emotion/react @emotion/styled

COPY . ./

RUN npm run build

# Stage 2: Serve the application
FROM httpd:2.4

# Copy the build output from the previous stage
COPY --from=build /app/dist /usr/local/apache2/htdocs/