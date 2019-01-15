lubasin apache ssl mooduli käsuga 
#
a2enmod ssl
#
aktiveersin default template
a2ensite default-ssl
#
service apache2 reload
#
mkdir /etc/apache2/ssl
#
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/apache2/ssl/apache.key -out /etc/apache2/ssl/apache.crt
#
chmod 600 /etc/apache2/ssl/*
#
nano /etc/apache2/sites-enabled/default-ssl.conf
#
Failis muutsin Servername: ja panin sinna 172.23.13.40:443
Allolevad read täiendasin järgmiselt
SSLCertificateFile /etc/apache2/ssl/apache.crt
SSLCertificateKeyFile /etc/apache2/ssl/apache.key
#
service apache2 reload

