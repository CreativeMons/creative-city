# Creative Mons (Creative City fork)

Run in development :

    $ composer update
    $ composer install
    $ php artisan migrate:reset --force
    $ php artisan migrate --force
    $ php artisan db:seed --force
    $ php artisan serve


## Vagrant

    $ vagrant up
    $ ssh vagrant@127.0.0.1 -p 2222
    # Perform migration & al on the Vagrant server
    $ vagrant halt

# Installation

## DEBIAN
     apt-get install libapache2-mod-php5 git php5-cli php5-curl php5-mysqlnd php5-gd \
     php-apc mysql-server php5-mcrypt php5-mysqlnd curl

## APACHE2
     a2enmod rewrite
     a2enmod negotiation

## COMPOSER
     curl -sS https://getcomposer.org/installer | php
     mv composer.phar /usr/local/bin/composer

## LARAVEL
     git clone https://github.com/micdevcamp/creative-city.git
     cd creative-city/
     composer install
     composer update
     chmod -R 0777 app/storage
     php artisan migrate:reset --force
     php artisan migrate --force
     php artisan db:seed --force
     chown -R www-data: public/system

# Configuration

## Database
     cp app/config/database.php.example app/config/database.php
     vi app/config/database.php

## Mail with Mandrill
     vi all/config/mail.php
