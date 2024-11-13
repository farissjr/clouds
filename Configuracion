1.Actualización de la máquina.

 Empieza por actualizar los repositorios y descargar las últimas actualizaciones disponibles.

 Actualiza el sistema utilizando el comando 'sudo apt update'.

 Actualizar paquetes con el comando "sudo apt upgrade" en la terminal.

 2.

 Configuración del servidor web Apache2 Para instalar el servidor web Apache, usa este comando: Instala Apache 2 con el comando: sudo apt install -y apache2.

 Para comprobar la instalación correcta de Apache, simplemente abre tu navegador y visita la dirección IP del servidor. Si has realizado correctamente la configuración, verás la página de inicio de Apache.

 Para instalar el servidor de bases de datos MySQL, simplemente sigue estos pasos.

 Para instalar MySQL Server, simplemente debes seguir los pasos de instalación indicados en el sitio web oficial.

 Instalar MySQL Server con el comando: sudo apt install -y mysql-server.

 Para utilizar PHP es necesario instalarlo junto con las bibliotecas requeridas.

 Después, procede a instalar PHP junto con las bibliotecas requeridas para su integración con Apache y MySQL.

 Instalar PHP y el módulo de Apache necesario con el siguiente comando: sudo apt install -y php libapache2-mod-php Instala PHP y sus extensiones necesarias en tu sistema utilizando el comando: sudo apt install -y php-fpm php-common php-mbstring php-xmlrpc php-soap php-gd php-xml php-intl php-mysql php-cli php-ldap php-zip php-curl.

 Reinicia Apache para que PHP se cargue correctamente.

 Reinicia el servicio de Apache 2 utilizando el comando:  sudo systemctl restart apache2 Configuración de la base de datos MySQL.

 Entra en la consola de MySQL: "Ingresa al sistema de gestión de base de datos MySQL con permisos de superusuario".

 Este párrafo es sencillo: 5.1. Creación de la base de datos: un proceso simple para construir una estructura organizada de datos.

 Crea una base de datos llamada bbdd (o el nombre que elijas) desde la consola de MySQL.

 Crear una base de datos llamada bbdd.

 Cinco punto dos. Crear un usuario en MySQL.

 Después, Registra un nuevo usuario con permisos para acceder a la base de datos. Se crea un usuario llamado usuario con la contraseña password y se le permite el acceso solo desde localhost.

 Crear un usuario llamado 'usuario' en la base de datos local utilizando la contraseña 'password'.

 El párrafo 5.3 es simple. Darle beneficios especiales al usuario.

 Para darle al usuario todos los privilegios necesarios para operar con la base de datos bbdd, usa este comando: Concede todos los permisos en la base de datos 'bbdd' al usuario 'usuario' en la dirección 'localhost'.

 Por último, cierra la consola de MySQL.

 Salida.

 Cinco con cuatro décimos. Verificar la conexión.

 Debes demostrar que puedes acceder a MySQL utilizando el nombre de usuario y la contraseña que has establecido.

 Iniciar sesión en MySQL con el usuario especificado y solicitar la contraseña.

 Permitir acceder a MySQL de forma remota.

 Normalmente, MySQL solo permite conexiones desde el servidor local. Si quieres que otras máquinas se conecten, tienes que cambiar la configuración.

 Seis punto uno. Cambiar la configuración de un archivo en MySQL.

 Modifica el archivo de configuración de MySQL para aceptar conexiones desde cualquier dirección IP, o solo desde una dirección IP en particular si es requerido. Usa un editor de texto, como vim, para abrir el archivo mysqld.cnf.

 Abre el archivo mysqld.cnf con el editor de texto Vim en la ubicación /etc/mysql/mysql.conf.d/.

 Encuentra la línea de dirección bind-address y modifícala a 0.0.0.0 para permitir conexiones desde cualquier máquina.

 Dirección de enlace = 0.0.0.

0 Por favor, guarda tus cambios y cierra el programa de edición.

 6.2. Es un número decimal. Reiniciar MySQL.

 Para que los cambios tengan efecto, es necesario reiniciar el servicio de MySQL.

 Reinicia el servicio de MySQL usando el comando: sudo systemctl restart mysql.

 Crear un usuario para acceder de forma remota.

 Para que un usuario pueda conectarse desde otra máquina (por ej., 192.168.22.100), primero debes crear un nuevo usuario y darle los privilegios necesarios.

 Crear usuario 'usuario' con contraseña 'password' y acceso desde la dirección IP '192.168.22.100' utilizando la autenticación nativa de MySQL.

 Después, se le dan permisos al nuevo usuario para acceder y modificar la base de datos bbdd.

 Conceder todos los permisos en la base de datos bbdd al usuario 'usuario' con dirección IP 192.168.22.100.

 Por último, sales de la consola de MySQL.

 Salida.

 8. Comprobación de la conexión a distancia.

 Intenta conectarte a MySQL desde una máquina remota utilizando el usuario y la contraseña previamente creados.

 Escriba mysql seguido de las opciones -u usuario -p -h para conectarse a la base de datos.

 Configuras Owncloud.

 Actualizar las listas de paquetes y descargar e instalar las actualizaciones disponibles.

 Primero verifica que tu sistema esté al día. Para actualizar las listas de paquetes e instalar las actualizaciones, simplemente ejecuta los comandos siguientes.

 Actualiza la lista de paquetes disponibles en tu sistema.

 Actualiza todos los paquetes del sistema sin necesidad de confirmación.

 9.2 Preparar la instalación de los requisitos del PPA.

 Necesitamos instalar un paquete extra para usar los paquetes de un PPA.  Este paquete se llama software-properties-common y ayuda a administrar las fuentes de software extra.

 Instala esto con: Instala el paquete "software-properties-common" utilizando el comando "sudo apt install -y".

 Nueve punto tres. Agregar el repositorio PPA de PHP de Ondřej Surý.

 Luego, hay que añadir el repositorio que tiene las versiones más recientes de PHP. El PPA de Ondřej Surý es muy popular para instalar versiones actuales de PHP en sistemas Debian/Ubuntu.

 Para añadir el PPA de PHP, simplemente ejecuta el comando que se muestra a continuación.

 Agregar el repositorio ppa:ondrej/php utilizando el comando sudo add-apt-repository ppa:ondrej/php -y con la configuración LC_ALL=C.UTF-8.

 Este comando añade el PPA a las fuentes de software de tu sistema.

 Actualizar los repositorios a la versión 9.4.

 Después de añadir el PPA, actualiza los repositorios para que el sistema pueda ver los nuevos paquetes disponibles en ese repositorio.

 Actualiza la lista de paquetes disponibles en el sistema.

 Instalar PHP versión 7.4 y las extensiones requeridas.

 Una vez configurados los repositorios, podemos instalar PHP 7.4 junto con las extensiones necesarias para su correcto funcionamiento en el servidor Apache.

 Para instalar PHP 7.

4, sigue estos pasos: Instalar PHP 7.4 usando el comando: sudo apt install php7.

4 -y Colocar el módulo de PHP en Apache (mod_php): Instalar PHP y el módulo de PHP para Apache con la versión 7.4 usando el comando 'sudo apt install -y php libapache2-mod-php7.4'.

 Se requiere instalar las extensiones de PHP 7.4 para poder utilizar diferentes funcionalidades.

 Instala los siguientes paquetes PHP en tu sistema: php7.4-fpm, php7.4-common, php7.4-mbstring, php7.4-xmlrpc, php7.4-soap, php7.4-gd, php7.4-xml, php7.4-intl, php7.4-mysql, php7.4-cli, php7.4-ldap, php7.4-zip y php7.4-curl, sin pedir confirmación.

 Estas extensiones ofrecen una amplia gama de funciones útiles, como compatibilidad con bases de datos MySQL, edición de imágenes, gestión de archivos XML, entre otros.

 9.

6 Elegir la versión principal de PHP Si tienes múltiples versiones de PHP en tu servidor, puedes elegir cuál quieres usar como la principal.

 Usa el siguiente comando para lograrlo: Cambiar la versión de PHP en el sistema mediante el comando "sudo update-alternatives --config php" Con este comando podrás ver las versiones de PHP que tienes en tu sistema. Escribe el número de la versión de PHP que deseas fijar como predeterminada, por ejemplo, PHP 7.4.

 Activar los módulos de Apache requeridos para PHP 7.4.

 Para que Apache pueda procesar de manera adecuada las solicitudes de PHP 7.4, necesitas activar ciertos módulos y ajustes de configuración.

 Se requieren los siguientes módulos: Debes activar los módulos proxy_fcgi y setenvif.

 Ejecuta el comando "sudo a2enmod proxy_fcgi setenvif" para habilitar los módulos de Apache proxy_fcgi y setenvif.

 Activar la configuración de php7.4-fpm.

 Habilitar la configuración de PHP7.4-FPM.

 Para reiniciar Apache2, simplemente es necesario ejecutar el comando 9.8.

 Es importante reiniciar Apache después de hacer cambios para que los ajustes sean aplicados correctamente. Para reiniciar Apache, utiliza el siguiente comando.

 Reinicia el servicio de Apache con el comando: sudo service apache2 restart.
Después, transfieres los archivos de la aplicación web al servidor.

 Primero, asegurémonos de tener el archivo comprimido de la aplicación web en un lugar fácil de encontrar. En este caso, el archivo app-web.zip se ha descargado en la carpeta ~/Descargas. Si el idioma de tu sistema es distinto, necesitarás ajustar el comando según la ruta en tu idioma.

 Diez punto uno. Mueve el archivo al directorio de Apache.

 Para mover el archivo comprimido de la aplicación web al directorio principal de Apache, usa el comando: Copia el archivo "app-web.zip" que está en la carpeta de descargas a la carpeta de directorio web en la ruta "/var/www/html" usando el comando "sudo cp".

 Si no encuentras la carpeta "Descargas", asegúrate de cambiar la ruta del comando para reflejar dónde guardaste el archivo ZIP.

 10.2 es un número decimal. Ingresar al directorio de Apache.

 Después, ingresamos al directorio /var/www/html utilizando el comando: Cambiar al directorio html en la ruta /var/www.

 El párrafo es demasiado corto para ser reescrito, ya que solo contiene un número y un punto. No hay suficiente información para poder realizar una reescritura significativa. Extraer el archivo ZIP.

 Utiliza este comando para extraer el archivo ZIP que contiene la aplicación web: Descomprimir app-web.zip.

 Esto extraerá el contenido del archivo ZIP en la carpeta actual /var/www/html.

 El 10 de abril. Colocar los archivos en el lugar correcto.

 Después, trasladamos los archivos extraídos de la carpeta app-web a la carpeta principal /var/www/html. Debes cambiar el nombre de la carpeta descomprimida para que coincida con la que se creó al descomprimir el archivo.

 Copia todos los archivos y carpetas de la carpeta "app-web" al directorio actual. El directorio /var/www/html es una ubicación común para alojar archivos de un sitio web en un servidor.

 Diez punto cinco. Borra la carpeta que descomprimiste.

 Después de copiar los archivos correctamente, puedes borrar la carpeta descomprimida (app-web) para mantener tu sistema ordenado.

 Eliminar de manera forzada y recursiva el directorio llamado "app-web".

 El número 10.6. es un número decimal que se representa por la combinación del número entero 10 y la fracción decimal 0.6. Borrar el archivo index.html por defecto de Apache.

 A veces, el archivo index.html predeterminado de Apache puede causar problemas al tratar de acceder a tu página web. Por esa razón, eliminamos este archivo para evitar problemas.

 Eliminar permanentemente el archivo index.html en la carpeta /var/www/html.

 Configurar quién puede acceder y modificar los archivos de la aplicación web.

 Ahora que los archivos de la aplicación web están en /var/www/html, se deben establecer los permisos correctos para que Apache pueda acceder a ellos sin inconvenientes.

 Once con uno es igual a doce. : Configurar los permisos adecuados.

 Cambia los permisos de los archivos a 775 para que los propietarios y el grupo (Apache) puedan escribir, leer y ejecutar.

 Ve al directorio html dentro de www en var.

 Cambiar los permisos de todos los archivos y carpetas en este directorio para que tengan permisos de lectura, escritura y ejecución para el propietario, y permisos de lectura y ejecución para el grupo y para otros usuarios.

 El ejercicio 11.2 es fácil. Cambiar el dueño y grupo.

 Cambiar el propietario de los archivos a usuario y el grupo a www-data, que es el grupo utilizado por Apache en la mayoría de los sistemas Linux.

 Cambiar el propietario de todos los archivos y carpetas dentro del directorio actual a "usuario" y asignar el grupo "www-data".

 Esto garantiza que Apache tenga los permisos adecuados para servir los archivos y que el usuario (quien accede a la base de datos) pueda manipularlos según sea necesario.

 12. Entrar a la página web desde el navegador.

 Para comenzar, coloca los archivos de la aplicación en su lugar correspondiente y ajusta los permisos necesarios.

 Luego, abre tu navegador web e ingresa a la dirección: Accede a la dirección web: http://localhost Si estás accediendo desde una computadora diferente, cambia "localhost" por la dirección IP de tu servidor.

 Debes visitar la página de instalación de la app web. Si la configuración es correcta, se mostrará el asistente de instalación, el cual solicitará datos acerca de la base de datos y del usuario administrador.

 Establecer la base de datos en la página web.

 Durante la instalación de la aplicación web, deberás ingresar la información de la base de datos solicitada. Asegúrate de incluir la siguiente información.

 El usuario de la base de datos es simplemente "usuario".

 La contraseña para acceder a la base de datos es "password".

 Base de datos: sistema de almacenamiento de información.

 Localhost es el nombre de dominio que se utiliza para referirse al propio equipo en el que se está trabajando, es decir, a la computadora personal en la que se encuentra el usuario.

 Con esta información, la aplicación podrá conectarse con éxito a la base de datos MySQL que previamente configuramos.

 Crear un administrador de usuario.

 En la siguiente ventana, el instalador de la aplicación te solicitará crear un usuario administrador para poder acceder a ella. Por favor, ingresa tu nombre de usuario y contraseña, elige los que desees y luego guarda los cambios.

  Terminar la instalación.

 Después de configurar la base de datos y crear un usuario administrador, la instalación de la aplicación web estará lista.

 Ahora puedes entrar a la aplicación en todo momento usando la dirección web:  .

 http://localhost
  .
