### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:15-alpine3.21
# COMPLETAR

```
docker run -d --name Postgres-web -e POSTGRES_PASSWORD=admin postgres:15-alpine3.21
```

### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4

# COMPLETAR
```
docker run -d --name pgadmin -e PGADMIN_DEFAULT_EMAIL=admin@admin.com -e PGADMIN_DEFAULT_PASSWORD=admin -p 8080:80 dpage/pgadmin4
```
La figura presenta el esquema creado en donde los puertos son:
- a: (completar con el valor)
- b: (completar con el valor)
- c: (completar con el valor)

![Imagen](esquema-2-ejercicio.PNG)

## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.
# COMPLETAR CON UNA CAPTURA DEL LOGIN
<img width="1916" height="1150" alt="image" src="https://github.com/user-attachments/assets/da91465d-a358-4b19-a498-6f75d6cbab1c" />

**Depúes del login**
<img width="1918" height="1104" alt="image" src="https://github.com/user-attachments/assets/3db15856-01a6-41ee-aebe-849c0becce50" />

### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.

**Crear Database** 
```
docker exec -it Postgres-web bash
psql -U postgres
CREATE DATABASE info;
```
**Crear Tabla** 
```
CREATE TABLE personas (
  id SERIAL PRIMARY KEY,
  nombre VARCHAR(100)
);
```
<img width="767" height="124" alt="image" src="https://github.com/user-attachments/assets/e54ba7fe-44c4-427b-9a14-61c9ba6f1dc8" />

## Desde el servidor postgresl
### Acceder al servidor
### Conectarse a la base de datos info
# COMPLETAR
```
\c info
```
### Realizar un select *from personas
# AGREGAR UNA CAPTURA DE PANTALLA DEL RESULTADO
<img width="995" height="240" alt="image" src="https://github.com/user-attachments/assets/60b98154-e43d-44ee-9983-b3aa712d6bb0" />


