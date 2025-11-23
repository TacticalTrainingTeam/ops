FROM php:7.3.33-apache

# Use the default production configuration
RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"

# Enable Apache Rewrite module
RUN a2enmod rewrite

# Docker PHP Extension Installer https://github.com/mlocati/docker-php-extension-installer
ADD --chmod=0755 https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

# Drupal 7 PHP Requirements https://www.drupal.org/docs/7/system-requirements/php-requirements-for-drupal-7
RUN install-php-extensions mysqli pdo_mysql gd imagick opcache