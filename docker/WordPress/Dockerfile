FROM wordpress:php7.3-apache

# Enable apache vhosts
# COPY ./vhosts/app.conf /etc/apache2/sites-available/000-app.conf
# COPY ./vhosts/phpmyadmin.conf /etc/apache2/sites-available/000-phpmyadmin.conf

# Install xdebug
RUN pecl install xdebug && docker-php-ext-enable xdebug

# Install Less for WP-CLI
RUN apt-get update && apt-get -y install less

# Install WP-CLI
RUN curl -s -o /usr/local/bin/wp \
    https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar \
    && chmod +x /usr/local/bin/wp

EXPOSE 80
EXPOSE 443