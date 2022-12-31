# ubuntulamp
Notes about LAMP on Ubuntu 22.04. How to's, etc.

## Apache 2
sudo apt install apache2

#test with curl, output is html source

curl http://localhost or curl http://<<machine-ip-address>>

## MySQL Server
  
sudo apt install mysql-server

sudo mysql 

#set mysql root password to Mysqlroot123!
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Mysqlroot123!';
exit;

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

#test with curl, output is php info page

curl http://localhost or curl http://<<machine-ip-address>>
