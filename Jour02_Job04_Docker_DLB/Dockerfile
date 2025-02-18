# Start my image with an Apache and PHP base image
FROM php:7.4-apache

# Copy the index.php file in the Apache directory
COPY index.php /var/www/html/


# Expose the port 8080
EXPOSE 8080

# Start the apache app using foreground status to keep it active
CMD ["apache2-foreground"]