laksin html kausta 
#
cd /var/www/html
#
laadisin alla koige uuemad wordpress failid
#
wget http://wordpress.org/latest.zip
#
installisin unzip'i et faile lahti pakkida
#
aptitude install unzip
#
unzip -q latest.zip
#
Seadsin õigused kaustadele
#
chown -R www-data:www-data /var/www/html/wordpress
#
chmod -R 775 /var/www/html/wordpress
#
tegin uue kausta wp-content kausta sisse
mkdir -p /var/www/html/wordpress/wp-content/uploads
#
Seadsin õigused uploads kaustale
#
chown -R www-data:www-data /var/www/html/wordpress/wp-content/uploads
#
#
tegin uue mysql andmebaasi
#
mysql -u root -p
#
CREATE DATABASE wordpress_sample;
#
CREATE USER wp_user@localhost IDENTIFIED BY 'password';
#
GRANT ALL PRIVILEGES ON wordpress_sample.* TO wp_user@localhost;
#
FLUSH PRIVILEGES;
#
exit
#
Peale seda installisin läbi brauseri wordpressi
