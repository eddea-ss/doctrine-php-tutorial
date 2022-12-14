# doctrine-php-tutorial
Doctrine + Symfony + Composer Tutorial

# Doctrine Composer-Symfony 

# Arch Distro install depends

    $ sudo pacman -S composer php wget pygtk xampp

    $ wget https://get.symfony.com/cli/installer -O - | bash

    $ sudo mv /home/eddea/.symfony5/bin/symfony /usr/local/bin/symfony\n

    $ sudo nano /etc/php/php.ini

    $ sudo pacman -S mysql

    $ sudo mariadb-install-db --user=mysql --basedir=/usr --datadir=/var/lib/mysql
    
    $ sudo mysql

# From mysql

    $ CREATE USER 'app'@'localhost' IDENTIFIED BY 'tecnoweb';
    $ GRANT ALL PRIVILEGES ON * . * TO 'app'@'localhost';
    $ FLUSH PRIVILEGES;

# Config new symfony

    $ symfony new doctrine

    $ composer require orm

    edit pass in "docker-compose" file

    edit ".env" file with your previous config 

# Traditional way

    $ CREATE DATABASE app;
    $ USE app;

# Doctrine

    $ php bin/console debug:config doctrine
    $ composer require --dev symfony/maker-bundle
    $ php bin/console doctrine:database:create

# create entity

    $ bin/console make:entity

# create migrations and execute

    $ bin/console doctrine:migrations:diff

    $ bin/console doctrine:migrations:migrate -n

    - migrations:execute --up 'DoctrineMigrations\\name'
    - migrations:execute --down 'DoctrineMigrations\\name'

# config type doctrine
    
    - ./config/packages/doctrine.yaml

# References

    - https://blog.pleets.org/article/instalar-apache-php-mysql-en-arch-linux
    - https://www.youtube.com/watch?v=336JTqgIMYk&list=PLWpsZlKx38t-iEAJCDwR2eEN6PM89pfQT&index=1
    - https://github.com/codenip-tech/codenip-symfony-doctrine/tree/feature/003-entities-and-migrations
    - https://www.youtube.com/watch?v=mCFy1r-4ZMU
    - https://www.youtube.com/watch?v=B3UQxTzlJlI
    - https://www.doctrine-project.org/projects/doctrine-orm/en/current/tutorials/getting-started.html
