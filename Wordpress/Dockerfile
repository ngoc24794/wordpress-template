FROM wordpress:php8.2-fpm

RUN pecl install xdebug

# Copy xdebug.ini to /usr/local/etc/php/conf.d/
COPY Wordpress/xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini

# Since this Dockerfile extends the official Docker image `wordpress`,
# and since `wordpress`, in turn, extends the official Docker image `php`,
# the helper script docker-php-ext-enable (defined for image `php`)
# works here, and we can use it to enable xdebug:
RUN docker-php-ext-enable xdebug