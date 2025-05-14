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

 2.1

