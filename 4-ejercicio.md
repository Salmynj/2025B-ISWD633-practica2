## Esquema para el ejercicio
![Imagen](esquema-4-ejercicio.PNG)

### Crear la red
# COMPLETAR
```
docker network create net-wp -d bridge
```
### Crear el contenedor mysql a partir de la imagen mysql:8, configurar las variables de entorno necesarias
# COMPLETAR
```
docker run -d --name mysql-contenedor --network net-wp -e MYSQL_ROOT_PASSWORD=admin -e MYSQL_DATABASE=admin -e MYSQL_USER=admin -e MYSQL_PASSWORD=admin mysql:8
``` 
### Crear el contenedor wordpress a partir de la imagen: wordpress, configurar las variables de entorno necesarias
# COMPLETAR
```
docker run -d --name Wordpress --network net-wp -p 8080:80 -e WORDPRESS_DB_HOST=mysql-contenedor:3306 -e WORDPRESS_DB_USER=admin -e WORDPRESS_DB_PASSWORD=admin -e WORDPRESS_DB_NAME=admin wordpress
```
De acuerdo con el trabajo realizado, en el esquema del ejercicio el puerto a es **(8080)**

Ingresar desde el navegador al wordpress y finalizar la configuración de instalación.
# COLOCAR UNA CAPTURA DE LA CONFIGURACIÓN
<img width="1854" height="1080" alt="image" src="https://github.com/user-attachments/assets/33552ddb-c46c-4ca4-aff6-c4dc587d1cdd" />

Desde el panel de admin: cambiar el tema y crear una nueva publicación.
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress
# COLOCAR UNA CAPTURA DEL SITO EN DONDE SEA VISIBLE LA PUBLICACIÓN.
<img width="1806" height="981" alt="image" src="https://github.com/user-attachments/assets/69c3b081-c948-40d2-b820-7f638fa32b1d" />

### Eliminar el contenedor wordpress
# COMPLETAR

### Crear nuevamente el contenedor wordpress
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress

### ¿Qué ha sucedido, qué puede observar?
# COMPLETAR

