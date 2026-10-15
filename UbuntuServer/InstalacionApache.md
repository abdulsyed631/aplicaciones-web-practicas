# Instalamos apache2

sudo apt-get install apache2

systemctl status apache2

cd /etc/apache2

Accede a la carpeta sites-available y edita el archivo 000-default.conf. Dentro de este fichero, busca la directiva DocumentRoot, la cual señala la ubicación de los archivos de la página web (por defecto es /var/www/html

Modifica o crea el archivo HTML dentro de esa ruta señalada; todo el contenido que guardes ahí se desplegará al abrir el sitio en el navegador.

# Desactivar la web de antes y poner la nueva en Apache

Hacemos una copia del archivo `000-default.conf` que está dentro de ``sites-available`` y le ponemos de nombre smr.conf

Abrimos ese archivo nuevo que acabamos de crear y en la parte de la ruta le ponemos ``/smr `` al final.

Ahora nos vamos al directorio ``/var/www/html`` y con el comando ``mkdir smr ``creamos una carpeta nueva que se llame así.

Entramos a esa carpeta nueva, abrimos un archivo con ``nano index.html`` y escribimos dentro el código HTML que queramos que salga en la pantalla.

Regresamos a la ruta de apache2, entramos en ``sites-available`` y apagamos la página vieja poniendo ``a2dissite 000-default.conf ``(o solo 00).

Aplicamos los cambios con ``systemctl reload apache2`` y miramos el status para ver si todo funciona bien.

Activamos nuestra página nueva escribiendo ``a2ensite smr.conf``, y otra vez volvemos a hacer el ``reload`` y a comprobar el status.

Volvemos a entrar al archivo ``smr.conf,`` cambiamos el puerto del VirtualHost al 7654 y recargamos de nuevo.

Por último, abrimos el archivo de puertos ``(ports.conf)` de apache2, escribimos abajo ``Listen 7654`` y hacemos el último reload para que coja el cambio
