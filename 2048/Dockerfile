# Using Ubuntu as the base image
FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
    git \
    nginx

# Cloning the 2048 game repository from GitHub
RUN git clone https://github.com/gabrielecirulli/2048.git /var/www/html/2048

RUN rm /etc/nginx/sites-enabled/default

COPY 2048-nginx.conf /etc/nginx/sites-enabled/

# Expose port 80 for Nginx
EXPOSE 80

# Starting Nginx
CMD ["nginx", "-g", "daemon off;"]
