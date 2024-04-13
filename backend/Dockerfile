# Use the official Node.js image from Docker Hub with version 21
FROM node:21

# Set the working directory inside the container to /app
WORKDIR /app

# Copy all files from the current directory (where Dockerfile is) into the container's /app directory
COPY . .

# Install Node.js dependencies using npm
RUN npm i

# Copy the .env.sample file from the current directory to .env inside the container
COPY .env.sample .env

# Expose port 5000 to allow outside connections to this port
EXPOSE 5000

# Define the default command to run when the container starts
CMD ["npm", "start"]
