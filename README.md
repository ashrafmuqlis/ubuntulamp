# ubuntulamp
Notes about LAMP on Ubuntu 22.04. How to's, etc.

## Apache 2
sudo apt install apache2

#test with curl, output is html source

curl http://localhost or curl http://vaagrant-vm-ip

## MySQL Server
  
sudo apt install mysql-server

sudo mysql 

#set mysql root password to Mysqlroot123!
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Mysqlroot123!';
exit;

## PHP Library

sudo apt install php libapache2-mod-php php-mysql

#test php engine
  
php -v

#test php web
  
sudo nano /var/www/html/index.php

#include the code below into index.php and save
  
"<?php
phpinfo();"

#configure apache index.* precedence. insert index.php after DirectoryIndex

sudo nano /etc/apache2/mods-enabled/dir.conf

#restart apache2
sudo systemctl reload apache2.service

#test with curl, output is php info page

curl http://localhost or curl http://<<machine-ip-address>>

Test this box with different PHP frameworks and applications. Happy Provisioning!

## Supplementary references

Learn to manage multiple domains/projects at the link below:

https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-22-04
