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
