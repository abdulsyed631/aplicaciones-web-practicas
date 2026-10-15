# Instalacion MARIADB PHP

# Objetivos
  Al terminar la práctica serás capaz de:
  • Explicar qué es una base de datos y para qué la necesita WordPress.
  • Instalar MariaDB sobre Ubuntu 24.04 y comprobar que funciona.
  • Instalar PHP y comprobar que Apache lo ejecuta.
  • Dejar el servidor (Linux, Apache, MariaDB y PHP) listo para instalar WordPress

Cómo encaja todo (el LAMP):
```Navegador --> Apache --> PHP --> MariaDB
(el visitante) (sirve la web) (ejecuta WordPress) (guarda los datos)
```
Ya tienes Linux y Apache. Hoy instalas las dos piezas que faltan: MariaDB y PHP

# PASO 1
```
sudo apt update
systemctl is-active apache2
```

# PASO 2
```
sudo apt install mariadb-server -y
```
Comprueba la versión instalada:
```mariadb --version```
Debes ver algo parecido a esto (el último número puede variar):
```mariadb Ver 15.1 Distrib 10.11.14-MariaDB, for debian-linux-gnu (x86_64)```


# PASO 3 
```
sudo systemctl status mariadb
systemctl is-enabled mariadb
```
(Active) running or enabled


# PASO 4
```sudo mariadb```
si todo esta bien apareceria esto :
```
Welcome to the MariaDB monitor. Commands end with ; or \g.
Server version: 10.11.14-MariaDB-0ubuntu0.24.04.1 Ubuntu 24.04
MariaDB [(none)]>
```

# COmandos principales
```
Comando Función
sudo systemctl start mariadb Arranca el servicio
sudo systemctl stop mariadb Detiene el servicio
sudo systemctl restart mariadb Reinicia el servicio
sudo systemctl status mariadb Muestra su estado
sudo systemctl enable mariadb Lo arranca automáticamente al encender el equipo                    (esta mal ignore )
```
 


# PASO 5
```
sudo systemctl stop mariadb
systemctl is-active mariadb
sudo mariadb
```





















