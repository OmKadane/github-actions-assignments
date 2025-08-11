# Use an official Node.js runtime as a parent image
FROM node:18-alpine

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy the built backend and frontend code from our artifacts
COPY ./backend/dist ./backend
COPY ./frontend/dist ./frontend

# Install backend dependencies
RUN cd backend && npm install --production

# Your app's start command
CMD [ "node", "backend/server.js" ]