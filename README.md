## PHP-FPM Docker Image ###

Docker container to install and run PHP-FPM.


###What is PHP-FPM ?###

PHP-FPM (FastCGI Process Manager) is an alternative FastCGI implementation for PHP.

###Getting image###
    
    docker pull komputronika/php-fpm

###Basic usage###
    
    docker run -v /path/to/your/app:/var/www/html -d komputronika/php-fpm

###Running your PHP script###

Run the PHP-FPM image, mounting a directory from your host.

    docker run -dit --name phpfpm -v /path/to/your/app:/var/www/html komputronika/php-fpm php index.php

or using Docker Compose:

    version: '2'
    services:
      php-fpm:
        container_name: php-fpm
        image: komputronika/php-fpm
        entrypoint: php index.php
        volumes:
          - /path/to/your/app:/var/www/html

###Installed extensions###
    bz2 
    iconv 
    mcrypt 
    mbstring 
    pdo_mysql 
    mysqli 
    zip
    
