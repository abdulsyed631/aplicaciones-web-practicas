# Paso 1 · Crear las carpetas y las páginas 

sudo mkdir -p /var/www/smr/web /var/www/smr/intranet      
    Con esto commando he creado la 2 carpetas en estos dirrectorio a la vez

echo "<huno> Intranet de SMR </huno>" | sudo tee /var/www/smr/intranet/intranet.html
    y con estos commando dos archivos del html

# Paso 2 Crear Usario de la internet 

sudo apt install apache2-utils -y
Sudo htpasswd -c /etc/apache2/.htpasswd alumno



# Paso 3 Decirle a pache que escuche en el puerto 9999
sudo nano /etc/apache2/ports.conf
    cuando estoy en este archivo añadir el listen 9999
    
____
# Paso 4 · Crear el virtualhost 
sudo nano /etc/apache2/sites -available/smr.conf    
    me vot aqui y pego este commando </h4> 

```
sudo cp /etc/apache2/sites-available/000-default.conf \
 /etc/apache2/sites-available/sitio1.conf
sudo mkdir -p /var/www/sitio1
echo '<h1>sitio1.local</h1>' | sudo tee /var/www/sitio1/index.html

```
    
    

  ```apache
<VirtualHost *:80>
    ServerName [www.smr.com](https://www.smr.com)
    DocumentRoot /var/www/smr/web
</VirtualHost>

<VirtualHost *:9999>
    ServerName [www.smr.com](https://www.smr.com)
    DocumentRoot /var/www/smr/intranet
    DirectoryIndex intranet.html

    <Directory /var/www/smr/intranet>
        AuthType Basic
        AuthName "Intranet SMR"
        AuthUserFile /etc/apache2/.htpasswd
        Require valid-user
    </Directory>
</VirtualHost>
```

# Reiniciar Apache

```
sudo a2ensite smr.conf | Activa el fichero smr.conf
sudo a2dissite 000-default.conf | Desactiva el fichero predeterminado
sudo apachectl configtest | Esto comprueba si hay errores en alguna sintaxis en los archivos de apache
sudo systemctl restart apache2 | Reinicia el sistema de apache
```

# Comprobacion


# UBUNTU




