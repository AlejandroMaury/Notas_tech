## Notas de linux con los comandos recientes y su función

### Para mysql
-1. Entrar al panel mysql desde la terminal
-mysql -u root -p


-2. **Revisar el listado de usuarios** 
-SELECT user FROM mysql.user GROUP BY user;


-3. **Agregar un usuario** 
-CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password'; con contraseña
-CREATE USER 'newuser'@'localhost'; sin contraseña
-GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'localhost'; esto se realiza para dar privilegios de uso sobre la BDD

Los asteriscos en este comando se refieren a la base de datos y la tabla (respectivamente) a los que pueden acceder.
Este comando específico permite al usuario leer, editar, ejecutar y realizar todas las tareas en todas las bases de datos y tablas.
Tenga en cuenta que en este ejemplo estamos otorgando a newuser acceso de root completo a todo en nuestra base de datos.
Si bien esto es útil para explicar algunos conceptos de MySQL, puede ser poco práctico para la mayoría de casos de uso y podría poner la seguridad de su base de datos en alto riesgo.
Una vez que haya finalizado los permisos que desea configurar para sus nuevos usuarios, asegúrese siempre de volver a cargar todos los privilegios.

-FLUSH PRIVILEGES;

-4. **Eliminar un usuario**
-DELETE FROM mysql.user WHERE user = 'usuario';


5. 
