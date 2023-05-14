FROM nginx:latest

# Install additional packages
RUN apt-get update -y && apt-get install -y procps


RUN mkdir -p /www

# Set permissions for non-root user
RUN chown -R 1000:1000 -R /www

# Change user
USER 1000

RUN mkdir /tmp/logs

# Expose port 80
EXPOSE 80

# Start NGINX
CMD ["nginx", "-g", "daemon off;"]

