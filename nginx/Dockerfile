# Use the official NGINX image from Docker Hub
FROM nginx:latest

# Remove the default nginx.conf and default sites-enabled configurations
RUN rm /etc/nginx/conf.d/default.conf

COPY ./nginx/proxy_params /etc/nginx/proxy_params

# Copy the custom nginx.conf from the current directory to the container
COPY ./nginx/nginx.conf /etc/nginx/nginx.conf

# Copy the custom site configuration from your project to the sites-enabled directory
COPY ./nginx/myproject /etc/nginx/sites-enabled/myproject

# Expose port 80 to the outside world
EXPOSE 80

# Start NGINX using the default command defined in the base image
CMD ["nginx", "-g", "daemon off;"]

