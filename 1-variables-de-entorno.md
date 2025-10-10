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

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

### ¿Qué bases de datos existen en el contenedor creado?
# COMPLETAR
```
show databases;
```

