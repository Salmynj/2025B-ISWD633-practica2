### COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado al realizar la práctica también se debe documentar.

Consultar: Cómo se gestionan datos confidenciales con los secretos de Docker (Docker Secrets).

# Consulta 
**Cómo se gestionan datos confidenciales con los secretos de Docker (Docker Secrets).** 

En el desarrollo de aplicaciones es normal que se majene información sensible como contraseñas, llaves Api, credenciales de bases de datos, etc.

Para evitar exponer estos datos en los archivos o imagenes de docker, se utiliza una herramienta integrada llamada `Docker secrets` que permite gestiornar de manera segura la información confidencial dentro de los contenedores.

### ¿Qué son Docker Secrets?
Los docker secrets son una funcionalidad que ofrece Docker para gestionar datos con información sensible de manera centralizada y transmitirlos de forma segura, unicamente a los contenedores que nececsiten acceder a ellos. 
Los `secrets` se cifran deurante el transito y en reposo en un ejambre de Docker **(Docker swarm)**. 

De manera que los secretos se guardan cifrados en el sistema de docker y se comparten únicamente con los servicios (modo Swarm)que los necesiten evitando que queden visibles en variables de entorno, imágenes o volúmenes. 

Conociendo lo anterior podemos responder la pregunta de la consulta como una secuencia de pasos: 
Para gestionar los docker secrets... 

**1.** Se crea el secreto utilizando el comando `docker secret create`

**2.** Usamos el secreto en un servicio ejecutado en modo swarm. 
En este paso el secreto se monta automáticamente como un archivo de solo lectura en la ruta `/run/secrets/`. 

**3.** Visualizamos el secreto con `docker secret ls` tambien podemos eliminar un secreto con `docker secret rm`. 

