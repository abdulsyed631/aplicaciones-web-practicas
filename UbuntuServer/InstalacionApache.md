# Instalamos apache2

sudo apt-get install apache2

systemctl status apache2

cd /etc/apache2

Accede a la carpeta sites-available y edita el archivo 000-default.conf. Dentro de este fichero, busca la directiva DocumentRoot, la cual señala la ubicación de los archivos de la página web (por defecto es /var/www/html

Modifica o crea el archivo HTML dentro de esa ruta señalada; todo el contenido que guardes ahí se desplegará al abrir el sitio en el navegador.

# Desactivar la web de antes y poner la nueva en Apache

Hacemos una copia del archivo `000-default.conf` que está dentro de `sites-available`` y le ponemos de nombre smr.conf
