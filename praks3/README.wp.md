lisasin /etc/apt/sources.list faili: deb http://packages.dotdeb.org jessie all
deb-src http://packages.dotdeb.org jessie all
#
salvestasin ja apt update
#
apt install php7.0-cli php7.0-curl php7.0-dev php7.0-zip php7.0-fpm php7.0-gd php7.0-xml php7.0-mysql php7.0-mcrypt php7.0-mbstring php7.0-opcache
#
laksin /tmp/ kausta ning laadisin alla mysql conf'i 
wget https://dev.mysql.com/get/mysql-apt-config_0.8.9-1_all.deb
#
dpkg -i mysql-apt-config_0.8.9-1_all.deb käsuga pakkisin faili lahti ja valisin konfiguratsioonist versiooni 5.6
#
apt-update
apt install mysql-community-server
määrasin root kontole parooli
user=root
password=qwerty
#
aptinstall phpmyadmin
nano /etc/apache2/apache2.conf --> Include /etc/phpmyadmin/apache.conf
systemctl restart apache2
# Peale seda sain ligi phpmyadmin lehele
user=root
password=qwerty

tegin var/www/public_html kausta faili test.php mis väljastab minnes lehele 172.23.13.40/~it/test.php tekstina "test v2"
varem sai tehtud ka test.php fail kuhu lisasin <?php phpinfo(); ?> mis väljastab olemasoleva php info
