<h3> Paso 1 · Crear las carpetas y las páginas </h3>

sudo mkdir -p /var/www/smr/web /var/www/smr/intranet      
    Con esto commando he creado la 2 carpetas en estos dirrectorio a la vez

echo "<huno> Intranet de SMR </huno>" | sudo tee /var/www/smr/intranet/intranet.html
    y con estos commando dos archivos del html

<h3> Paso 2 Crear Usario de la internet </h3>

sudo apt install apache2-utils -y
Sudo htpasswd -c /etc/apache2/.htpasswd alumno



<h3>Paso 3 Decirle a pache que escuche en el puerto 9999</h3>
sudo nano /etc/apache2/ports.conf
cuando estoy en este archivo añadir el listen 9999



