# Pasos para instalar PHP 7.4 en Ubuntu 24.04 y preparar ownCloud



1.1 **primero bajarse el .zip de ownCloud Server**

![image](https://github.com/user-attachments/assets/a0e6e5ed-c7cd-4477-a7b5-45f2e3c1032b)


1.2 **Este paquete permite añadir nuevos repositorios al sistema.
Como PHP 7.4 ya no está en los repos oficiales de Ubuntu 24.04, necesitamos este comando para poder agregar un repositorio externo donde sí esté.**

![captura1](https://github.com/user-attachments/assets/4cf29df8-d2ae-442a-96c5-956e1f0fc7c6)


1.3 **Este repositorio contiene versiones antiguas y nuevas de PHP. Añadirlo es necesario para poder instalar PHP 7.4, ya que no viene incluido por defecto en Ubuntu 24.04. El LC_ALL=C.UTF-8 evita errores de codificación al ejecutar el comando.**
![2](https://github.com/user-attachments/assets/c5b28e89-3222-4c6b-9937-1e92d6694931)



1.4 **Después de añadir el nuevo repositorio, usamos este comando para que Ubuntu lo reconozca y actualice la lista de todos los programas que puede instalar. Así ya podremos instalar PHP 7.4.**


![3](https://github.com/user-attachments/assets/c51925ad-eb90-4986-9703-b693790bc611)


1.5 **Con este comando instalamos la versión básica de PHP 7.4. Es necesaria porque ownCloud no es compatible con versiones más recientes como PHP 8.x.**


![4](https://github.com/user-attachments/assets/6ce8cdf9-0ad8-4545-8b50-822971959c15)


1.6 **Aquí instalamos el módulo que permite que Apache (el servidor web que usaremos) pueda ejecutar archivos PHP. Sin esto, Apache no podrá interpretar las páginas PHP correctamente.**


![5](https://github.com/user-attachments/assets/9406aee1-b3d1-46ef-b955-16d486da8a87)



1.7 **Estas extensiones son como herramientas extras que ownCloud necesita para funcionar bien. Por ejemplo: conexión con bases de datos (mysql), compresión de archivos (zip), carga de imágenes (gd), entre otros.**

![6](https://github.com/user-attachments/assets/bc099f47-529b-4f76-a9db-02cd4e8ed25c)



1.8 **Este comando sirve para escoger qué versión de PHP usará el sistema si hay varias instaladas. Aquí seleccionamos la 7.4 para asegurarnos de que todo funcione con ownCloud.**

![7](https://github.com/user-attachments/assets/31875727-0c4f-4fb3-ad0e-a14bdec9fa29)



1.9 **Estos módulos son necesarios para que Apache pueda comunicarse bien con PHP-FPM, que es una forma más rápida y eficiente de ejecutar PHP.**

![8](https://github.com/user-attachments/assets/3f80767d-7b35-4f42-9cf8-d9257ad8f5dc)



2.0 **Este comando carga la configuración especial de PHP 7.4 en Apache para que el servidor sepa cómo manejarlo.**

![9](https://github.com/user-attachments/assets/fcfe68ad-8e7e-407d-9c7d-b652d8b38269)




 # Instalacion de apache2, mysql i algunas librerias al contenido

 2.1 **Con apt update y apt upgrade nos aseguramos de tener todos los paquetes al día antes de instalar nada.**


![image](https://github.com/user-attachments/assets/a109b45a-c207-4525-9af1-695815603a91)


![image](https://github.com/user-attachments/assets/5242a7af-fbd5-4f0e-846d-445dbbe77d2d)



2.2 **Instalamos Apache2**
**Este comando instala el servidor web Apache, que será el encargado de mostrar las páginas en el navegador.**


![image](https://github.com/user-attachments/assets/604bfe5d-dd2d-4b88-afbb-e5e2cbc05e05)



2.3 **Instalamos MySQL**
**Instalamos el sistema de bases de datos MySQL, necesario para gestionar la información de las aplicaciones web.**



![image](https://github.com/user-attachments/assets/fab52682-412a-4ff5-87dc-6d58b051e376)



2.4 **Instalamos PHP y sus librerías**
**Aquí instalamos PHP y varios módulos importantes para que funcione bien con Apache y MySQL.**



![image](https://github.com/user-attachments/assets/0f6788ea-99d7-433a-b0d3-fe0784d603cf)



2.5 **Instalamos PHP**
**Aquí instalamos PHP y varios módulos importantes para que funcione bien con Apache y MySQL..**



![image](https://github.com/user-attachments/assets/d69ea7b1-aae7-48f6-aad7-d1f5945f05ef)




2.6 **Reiniciamos Apache**
**Reiniciamos el servidor para aplicar todos los cambios y cargar correctamente los módulos de PHP.**


![image](https://github.com/user-attachments/assets/caa77b65-5ab2-4406-aabb-c55497939ec3)




2.7 Copiamos el archivo de la aplicación web
Usamos sudo cp ~/Baixades/app-web.zip /var/www/html para mover el archivo .zip al directorio donde se alojará la web. Sustituye el nombre si el archivo se llama distinto o si tu carpeta de descargas no es Baixades.

![1](https://github.com/user-attachments/assets/46dadd26-bba2-4431-a7b1-6e13e44fb23a)




2.8 Entramos en el directorio web
Con cd /var/www/html accedemos a la carpeta principal donde se guardan los archivos que servirá Apache.


![2](https://github.com/user-attachments/assets/e84c9075-56d4-4cb0-90c2-d9c054580bc4)


2.9 Descomprimimos el archivo
Usamos sudo unzip app-web.zip para extraer el contenido del archivo ZIP de la aplicación.

![3](https://github.com/user-attachments/assets/465134aa-b72f-46e6-80d2-6a6e0a68964e)


3.0 Copiamos los archivos al directorio raíz de la web
Con sudo cp -R app-web/. /var/www/html movemos todo el contenido descomprimido directamente al directorio principal.


![4](https://github.com/user-attachments/assets/a3970830-8989-4ec3-b664-499e55c957d4)


3.1 Eliminamos la carpeta original descomprimida
Ejecutamos sudo rm -rf app-web/ para borrar la carpeta ya vacía y no dejar archivos duplicados.

![5](https://github.com/user-attachments/assets/914e84d8-ebb1-4fc9-ada8-b3343fa23edd)


3.2 Borramos el archivo index.html por defecto
Apache trae un archivo de inicio por defecto. Lo eliminamos con sudo rm -rf /var/www/html/index.html para que no interfiera.
![6](https://github.com/user-attachments/assets/5afc9cd0-2f56-4ee9-920a-558ea3f3dc66)


3.3 Aplicamos permisos a los archivos de la web
Con sudo chmod -R 775 . damos permisos adecuados, y con sudo chown -R usuario:www-data . cambiamos el propietario al usuario actual y al grupo de Apache.

![7](https://github.com/user-attachments/assets/e1e5c3d4-a384-4737-8c29-8e36d2772041)

 


3.4Con sudo chmod -R 775 . damos permisos de lectura, escritura y ejecución al propietario y grupo, y lectura y ejecución para otros usuarios.


![8](https://github.com/user-attachments/assets/f664100d-f64f-4e84-b522-f3b9b9bf1345)


3.5 Cambiamos el propietario de los archivos
Con sudo chown -R usuario:www-data . asignamos como propietario al usuario actual (usuario) y como grupo a www-data, que es el grupo usado por Apache para acceder a los archivos.


![9](https://github.com/user-attachments/assets/be41d622-e5d3-417c-9d74-569be645bba3)

