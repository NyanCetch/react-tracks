# Production

# Multi-stage build

# Stage 1 - Build
# FROM node:alpine as builder
# WORKDIR /app
# COPY package*.json ./
# RUN npm ci
# COPY . .
# RUN npm run build

# # Stage 2 - Copy build
# FROM node:alpine
# RUN yarn global add serve
# WORKDIR /app
# COPY --from=builder /app/build .
# EXPOSE 3000
# CMD ["serve", "-p", "3000", "-s", "build"]

# Development 

# # Use an official node runtime as a parent image
FROM node:12

WORKDIR /app/

# Install dependencies
# COPY package.json yarn.lock /app/

# Add rest of the client code
COPY . /app/
RUN npm install

EXPOSE 3000

ENTRYPOINT npm run start