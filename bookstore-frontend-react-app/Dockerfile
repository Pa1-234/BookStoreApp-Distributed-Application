# Use the official Nginx base image
FROM nginx:latest

# Set the working directory to the Nginx web root
WORKDIR /usr/share/nginx/html

# Copy the built React app files into the container
COPY build/ .

# Expose port 80 to the outside world
EXPOSE 80

# Default command to run when the container starts
CMD ["nginx", "-g", "daemon on;"]
