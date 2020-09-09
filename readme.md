The following are the packages and rights I use for install processing on a Ubuntu 18.04

#install apache 2
sudo apt install apache2 - y

#install PHP 7.2 and required extensions 
sudo apt install php7.2 php7.2-gd php7.2-zip -y

#enable zipArchive 
sudo cat /etc/php/7.2/apache2/php.ini

#Add the following to php.ini 
extension=zip.so

#enable mod rewrite 
sudo a2enmod rewrite

#install Maria DB and PHP tools
sudo apt install mariadb-server php-mysql -y

#restart Apache2 
sudo systemctl restart apache2

#SQL secure installatino 
sudo mysql_secure_installation

#Log in MariaDB
sudo mysql

#In the SQL console
#Create Database (Change the database name)
Create database [database name];

#Create User (Change username and password)
CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';

#Grant all right of the user (Change database and username)
Grant all privileges [database] on ‘newuser’@’localhost’;

#Update privileges 
flush privileges; 

#Exit SQL console; 
exit