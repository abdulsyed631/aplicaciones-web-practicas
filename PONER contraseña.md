# Paso 1
"
'''
sudo a2enmod auth_basic
sudo systemctl restart apache2
'''

# Paso 2 Crear el usuario y la contraseña
'''
sudo htpasswd -c /etc/apache2/.htpasswd admin
'''

# Paso 3
'''
sudo nano /var/www/html/.htaccess
'''

# Paso 4

'''
AuthType Basic
AuthName "Privado"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
'''

sudo htpasswd -c /etc/apache2/.htpasswd smr

Protect only smr.html
Open the Apache configuration:
sudo nano /etc/apache2/sites-available/000-default.conf

Inside <VirtualHost *:80>, add:
'''
<Directory /var/www/html>
    <Files "smr.html">
        AuthType Basic
        AuthName "SMR"
        AuthUserFile /etc/apache2/.htpasswd
        Require valid-user
    </Files>
</Directory>
'''

restart apche

sudo systemctl reload apache2


