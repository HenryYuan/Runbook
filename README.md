# Runbook
Installing wordpress with ubuntu 16.04 on the server

Step1 - Connect to your server
ssh username@domain.com -p port

Step2 - install apache2
sudo apt-get install apache2
chown -R username xxx/xxx/root

Step3 - install MYSQL
sudo apt-get update
sudo apt-get install mysql

Step4 - install PHP
sudo apt-get install php7.2
sudo apt-get install php7.2-mysql
sudo apt-get install php7.2-mbstring
sudo apt-get install libapache2-mod-php7.2
sudo service apache2 reload

Step5 - install Wordpress
cd to your root
curl -0 https://wordpress.org/latest.zip
sudo apt-get install unzip
unzip latest.zip

Step6 - setup
cd to wordpress
sudo mv wp-config-sample.php wp-config.php
sudo nano wp-config.php
change to this
define('DB_NAME', 'wordpress_db');
define('DB_USER', 'wordpress_user');
define('DB_PASSWORD', 'PASSWORD');
define('DB_HOST', 'localhost');
define('DB_CHARSET', 'utf8');
define('DB_COLLATE', '');

Finished installed Wordpress
