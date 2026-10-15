# Instalamos apache2

sudo apt-get install apache2
systemctl status apache2
cd /etc/apache2

Accede a la carpeta sites-available y edita el archivo 000-default.conf. Dentro de este fichero, busca la directiva DocumentRoot, la cual señala la ubicación de los archivos de la página web (por defecto es /var/www/html
