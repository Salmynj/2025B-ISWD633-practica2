# Variables de Entorno
### ¿Qué son las variables de entorno?
# COMPLETAR
```
Las variables de entorno son valores que se almacenan en el sistema operativo que pueden ser utilizados por programas o procesos que se estan ejecutando. 
```
### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

# COMPLETAR
```
docker run -d --name contenedor -e username=1234 -e role=admin nginx:alpine
```
# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR
<img width="1112" height="75" alt="image" src="https://github.com/user-attachments/assets/5f90cc20-2a64-4867-a387-06400748ca1f" />

### Crear un contenedor con la imagen de mysql, mapear todos los puertos
# COMPLETAR
```
docker run -P -d --name Mysql-web mysql
```
### ¿El contenedor se está ejecutando?
# COMPLETAR
```
No se esta ejecutando
```
### Identificar el problema
# COMPLETAR
```
docker logs Mysql-web
```
<img width="1384" height="299" alt="image" src="https://github.com/user-attachments/assets/9580883b-981d-4c74-9d7c-a2a85bd54349" />

### Contenedor creado con la variable de entorno MYSQL_ROOT_PASSWORD

```
docker run -P -d --name Mysql-web1 -e MYSQL_ROOT_PASSWORD=1234 mysql
```

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

### ¿Qué bases de datos existen en el contenedor creado?
# COMPLETAR

```
docker exec -it Mysql-web1 bash
mysql -u root -p
show databases;
```
<img width="502" height="292" alt="image" src="https://github.com/user-attachments/assets/2ca80cab-aebf-42a3-929d-de1b7eab0fc0" />

