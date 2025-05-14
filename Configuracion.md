1. Actualizar el Sistema
Primero, tienes que asegurarte de que tu sistema esté bien las últimas actualizaciones.Esto es importante para que todo funcione bien y no haya problemas de seguridad. 
Abre la terminal y pon estos comandos: 
sudo apt update 
sudo apt upgrade

2.Instalar Apache2
Apache es el servidor web que usaremos para que la página web funcione. Para instalarlo, escribe este comando en la terminal:

sudo apt install -y apache2
3. Cuando termine, abre tu navegador y entra en la IP de tu servidor. Si todo va bien deberías ver una página que dice algo como Bienvenido a Apache o simplemente apache

4. Instalar MySQL
MySQL es la base de datos donde vamos a guardar la información de la web. Instálalo con el siguiente comando:

sudo apt install -y mysql-server

5. Instalar PHP y las Librerías Necesarias
A continuación, instala PHP y las bibliotecas necesarias para integrarlo con Apache y MySQL
 ejecuta estos comandos:

sudo apt install -y php libapache2-mod-php
sudo apt install -y php-fpm php-common php-mbstring php-xmlrpc php-soap php-gd php-xml php-intl php-mysql php-cli php-ldap php-zip php-curl
6.Luego, reinicia Apache para que reconozca PHP:

sudo systemctl restart apache2

7. Configurar MySQL
Para empezar a usar MySQL, entra en la consola con

sudo mysql
8.Ahora, crea una base de datos. En este caso, la vamos a llamar bbdd, pero puedes poner cualquier nombre:

CREATE DATABASE bbdd;

9.Crear un Usuario en MySQL
Vamos a crear un usuario para que pueda acceder a la base de datos bbdd. Usa este comando:

CREATE USER 'usuario'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

10.Darle Privilegios al Usuario
Ahora le damos permisos  al usuario para que pueda trabajar con la base de datos:

GRANT ALL ON bbdd.* TO 'usuario'@'localhost';

11.Cuando termines, sal de MySQL:

exit 

12.Comprobar Conexión a MySQL
Para asegurarte de que todo funciona intenta conectarte a MySQL con el usuario que acabas de crear ahora mismo:

mysql -u usuario -p

13.Permitir Conexiones Remotas a MySQL
Si necesitas que otras máquinas se conecten a tu base de datos debes cambiar una opción en MySQL. por defecto solo permite conexiones desde el mismo servidor.

14. Modificar el Archivo de Configuración de MySQL
Para permitir conexiones desde otras IPs, abre el archivo de configuración de MySQL con:

sudo vim /etc/mysql/mysql.conf.d/mysqld.cnf

15. Busca la línea que dice bind-address y cámbiala a: 

bind-address = 0.0.0.0
Esto permitirá que cualquier máquina se conecte a tu base de datos. Guarda los cambios y cierra el archivo.

 16.Reiniciar MySQL
Para que los cambios tengan lo suyo, reinicia MySQL:

sudo systemctl restart mysql

17.Crear un Usuario para Conexión Remota
Si quieres que un usuario se conecte desde otra máquina como por ejemplo con la IP 192.168.22.100, puedes crear un usuario remoto con:

CREATE USER 'usuario'@'192.168.22.100' IDENTIFIED WITH mysql_native_password BY 'password';

Y le das permisos sobre la base de datos:

GRANT ALL ON bbdd.* TO 'usuario'@'192.168.22.100';

Luego sal de MySQL:

exit

18.Verificar Conexión Remota
Desde una máquina diferente puedes probar conectarte a MySQL con:

mysql -u usuario -p -h <IP_DEL_SERVIDOR_MYSQL>

19.Instalar OwnCloud 
Si quieres configurar una aplicación cOwnCloud Es una plataforma para almacenar archivos en línea.

20.Actualizar Paquetes
Primero asegúrate de que todo esté actualizado con los siguientes comandos:

sudo apt update
sudo apt upgrade -y

21.Instalar Requisitos Previos para PPA
Para agregar repositorios adicionales primero instala el paquete software-properties-common:

sudo apt install software-properties-common -y

22.Agregar el PPA de PHP
Para obtener la última versión de PHP necesitas agregar el repositorio de PHP de Ondřej Surý:

LC_ALL=C.UTF-8 sudo add-apt-repository ppa:ondrej/php -y

23.Actualizar los Repositorios
Una vez agregado el PPA actualiza los repositorios de tu sistema:

sudo apt update

24.Instalar PHP 7.4 y las Extensiones Necesarias
Ahora instala PHP 7.4 y las extensiones necesarias para que funcione correctamente con Apache:

sudo apt install php7.4 -y
sudo apt install -y php libapache2-mod-php7.4
sudo apt install -y php7.4-fpm php7.4-common php7.4-mbstring php7.4-xmlrpc php7.4-soap php7.4-gd php7.4-xml php7.4-intl php7.4-mysql php7.4-cli php7.4-ldap php7.4-zip php7.4-curl

25.Seleccionar PHP 7.4 como Predeterminado
Si tienes varias versiones de PHP selecciona PHP 7.4 como la predeterminada:

sudo update-alternatives --config php


26.Activar los Módulos Necesarios en Apache
Para que Apache funcione bien con PHP 7.4 necesitas activar algunos módulos:

sudo a2enmod proxy_fcgi setenvif
sudo a2enconf php7.4-fpm

27.Reiniciar Apache
Después de hacer estos cambios reinicia Apache para que todo funcione correctamente:

sudo service apache2 restart

28.Copiar Archivos de la Aplicación Web
Ahora vamos a copiar los archivos de tu aplicación web al servidor. Si tienes un archivo comprimido por ejemplo, app-web.zip, usa este comando para copiarlo:

sudo cp ~/Descargas/app-web.zip /var/www/html

29. Descomprimir los Archivos
Accede al directorio donde se encuentran los archivos de Apache:

cd /var/www/html

Y descomprime el archivo ZIP:

sudo unzip app-web.zip

30.Mover los Archivos a la Carpeta Correcta
Si la carpeta descomprimida tiene el nombre app-web, mueve los archivos a la raíz de /var/www/html con:

sudo cp -R app-web/. /var/www/html

31.Configurar Permisos
Asegúrate de que Apache pueda acceder a los archivos, estableciendo los permisos correctos:

sudo chmod -R 775 .
sudo chown -R usuario:www-data .

32. Acceder a la Aplicación Web
Finalmente, abre tu google y entra en  http://localhost o usa la IP de tu servidor si estás accediendo desde otro dispositivo.
Si todo está bien, deberías ver la página de instalación de tu aplicación web y listo ya tienes tu sistema actualizado.

33.Configurar la Base de Datos en la Aplicación
Durante la instalación de la aplicación te pedirá los datos de la base de datos rellena los datos con la siguiente información:

Usuario de la base de datos: usuario
Contraseña de la base de datos: password
Base de datos: bbdd
Dominio: localhost

34.Crear un Usuario Administrador
Luego la aplicación te pedirá que crees un usuario administrador. Pon el nombre y la contraseña que prefieras.

35.Finalizar la Instalación
Una vez hayas configurado todo, la instalación debería finalizar y podrás empezar a usar la aplicación y listo.




