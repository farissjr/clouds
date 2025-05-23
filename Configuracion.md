 # Configuració de MySQL


1 **Entramos en la consola de MySQL**
**Desde una terminal como root usamos sudo mysql para acceder al gestor de bases de datos.**

![1](https://github.com/user-attachments/assets/e9accb27-8247-4457-b5d4-2365c34b918a)




2 **Creamos la base de datos**
**Dentro de MySQL ejecutamos CREATE DATABASE bbdd; para crear una nueva base de datos llamada bbdd.**

![2](https://github.com/user-attachments/assets/318bd7dc-a1ba-4dbb-a92b-84fb2849d295)




3 **Creamos un usuario nuevo**
**Usamos CREATE USER 'usuario'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password'; para crear un usuario con acceso desde localhost.**

![3](https://github.com/user-attachments/assets/b9257de4-6ac2-4423-9a46-8584414d9f6f)





4 **Damos permisos al usuario**
**Con GRANT ALL ON bbdd.* TO 'usuario'@'localhost'; damos acceso total del usuario a la base de datos bbdd**

![4](https://github.com/user-attachments/assets/8ecca18c-e7e6-43a0-9632-cff20a308bc9)




5 **Salimos de MySQL**
**Escribimos exit para salir de la consola de MySQL.**

![5](https://github.com/user-attachments/assets/0fe5d473-354c-40c7-8c69-7987c5c3a4c2)




# Desenvolupament de la pràctica


6 **Abrimos el navegador para comprobar que todo funciona
Accedemos a http://localhost desde el navegador. Debería aparecer el instalador de la aplicación web que hemos descomprimido.**

![1](https://github.com/user-attachments/assets/0aa9be68-1666-4ce8-a673-8ef5baf15024)




7 **Configuramos la aplicación
En la pantalla de instalación, introducimos los datos necesarios para conectar con la base de datos y crear el usuario administrador.**

8 **Datos a introducir (según el manual):**

Usuario: usuario

Contraseña: password

Base de datos: bbdd

Dominio: localhost

![2](https://github.com/user-attachments/assets/46ca7e7a-1865-4641-b661-ceedd044f4ef)





9 **Ahora nos llevara al menu principal**

![3](https://github.com/user-attachments/assets/e8882af7-2012-46ca-9833-6e273f007316) 




10  # Demostracion de funcionamiento


**Usa la opción de crear carpeta nueva y ponle un nombre.**

![image](https://github.com/user-attachments/assets/46910531-21fc-4fd3-b53a-b489ee6d0d3b)






11 **Haz clic en un archivo o carpeta “Compartir” genera un enlace o asigna un usuario.**

 
![image](https://github.com/user-attachments/assets/4fd90b81-2508-489f-9534-1aa0e444d846)





12 **antes de hacer el anterior paso Ve al panel de administración “Usuarios” añade tres usuarios con roles distintos (administrador, editor, visualizador).**

![usuaris](https://github.com/user-attachments/assets/5b5c1a8b-a916-492a-a0de-280c947aa5db)


![ediotr y admin](https://github.com/user-attachments/assets/e73501d8-6933-4d8c-9fb5-91425680ca1a) 




13 **Para crear los usuarios tienes que clickar en la parte de ¨nombre de usuario¨ y en la de ¨correo electronico¨ una vez acabado le damos a CREAR**


![image](https://github.com/user-attachments/assets/38998ed0-8fe0-4a07-a4ef-fe421065ee4f)




14 **Ahora en la parte de ¨usuarios¨ a la esquina de la izuqierda saldra ¨agregar grupo¨ añadimos y asignamos cada grupo (administrador,editor,visualizador)**

![grupos](https://github.com/user-attachments/assets/525460aa-e835-4e59-82a2-f7270d2b2c21) 



15 **Volvemos a la crpeta clickamos en ¨compartidos¨ una vez dentro avamos a la seccion de ¨compartiendo¨ y le damos permisos de edicion o visualizador a los usuarios necesarios**

![image](https://github.com/user-attachments/assets/37a22bed-11a9-4345-b476-c6bee5de6422)




16 **Miramos si nos deja poner imagenes y documentos correctamente sin ningun problema**

![image](https://github.com/user-attachments/assets/3aaf91c8-5f45-4391-8f9b-cd411567337b) 



17 **Con los permisos que hemos dado anteriormente a los usuarios para eliminar editar y visualizar comprobamos si deja eliminar y editar**

![image](https://github.com/user-attachments/assets/59934a94-e9b4-4aea-a7c8-b9ae66bb9855)


![image](https://github.com/user-attachments/assets/c5cb847d-07c1-41df-8e78-ab80ef7489d5) 




18 **ahora Configuramos políticas de seguridad (caducidad de enlaces) y le ponemos contrasña (opcional)**

![image](https://github.com/user-attachments/assets/aa50f911-40e9-436d-861b-eae954acffcc)

![image](https://github.com/user-attachments/assets/f3c91e3c-971e-4474-a060-c44b609829b0) 


19 **Al acabar se nos creara automaticamente el enlace con contraseña para poder compartirlo entre usuarios y otras personas**

![image](https://github.com/user-attachments/assets/5048590d-507a-4a25-8cc4-e7f277af7e6c)

 
