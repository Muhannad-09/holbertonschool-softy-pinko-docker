# Use latest nginx as the base image
FROM nginx:latest

# Copy project files to the web root
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy custom nginx config
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf
