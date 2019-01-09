kirjutasin apt install apache2
laksin /var/www/html kataloogi ja kustutasin algse index.html faili ara ning kirjutasin uue
tegin tavakasutajale avaliku kausta: mkdir /home/it/public_html
linkisin selle /var/www kaustaga: ln -s /home/it/public_html /var/www
lubasin kaustad a2enmod userdir ja apache2 service restart
