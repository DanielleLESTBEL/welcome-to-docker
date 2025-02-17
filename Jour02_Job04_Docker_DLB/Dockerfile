# Start your image with an Apache and PHP base image
FROM php:7.4.3-apache

# Copy the index.php file in the Apache directory
COPY index.php /var/www/html/

# Copy local directories to the current local directory of our docker image (/app)

COPY ./Screenshots ./Screenshots

# Expose the port 8080
EXPOSE 8080

# Start the apache app using foreground status to keep it active
CMD [ "apache2-foreground", "build" ]