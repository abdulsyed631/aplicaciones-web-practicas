<h3> Paso 1 · Crear las carpetas y las páginas </h3>

sudo mkdir -p /var/www/smr/web /var/www/smr/intranet      
    Con esto commando he creado la 2 carpetas en estos dirrectorio a la vez

echo "<h1> Intranet de SMR </h1>" | sudo tee /var/www/smr/intranet/intranet.html
    y con estos commando dos archivos del html

Paso 2 Crear Usario de la internet 

sudo apt install apache2-utils -y
Sudo htpasswd -c /etc/apache2/.htpasswd alumno



<h3>Paso 3 Decirle a pache que escuche en el puerto 9999</h3>


