# Reflexión de Aprendizaje: Fundamentos de Docker

Hasta el momento, mi experiencia con Docker se había limitado a implementaciones bastante puntuales; lo utilizaba principalmente para levantar proyectos sencillos o consumir contenedores ya configurados sin profundizar demasiado en la mecánica interna del motor. Esta práctica me ha permitido entender "el porqué" detrás de los comandos, pasando de una ejecución mecánica a una comprensión real del ciclo de vida de las imágenes y los contenedores.

## Conceptos clave asimilados

Durante el desarrollo de estos ejercicios, he consolidado varios aspectos técnicos fundamentales:

* **Ciclo de vida y gestión:** Comprender la diferencia exacta entre descargar (`pull`), preparar (`create`), iniciar (`start`) y ejecutar directamente (`run`), así como la importancia del modo *detach* (`-d`) para no bloquear la terminal.
* **Redes y exposición de servicios:** El mapeo de puertos (`-p`) dejó de ser un simple comando para convertirse en un concepto claro de enrutamiento entre el host y el contenedor. Levantar servicios complejos como RabbitMQ (exponiendo tanto el *broker* como la interfaz de *management*) o Jenkins ilustró perfectamente esta capa de red.
* **Interacción y *Troubleshooting*:** Acceder a los contenedores mediante `docker exec` fue uno de los puntos más valiosos. Enfrentarme a errores reales de la terminal (como los conflictos de saltos de línea `\r` al no usar una terminal TTY, o el problema de traducción de rutas en Git Bash para Windows al buscar la contraseña de Jenkins) me dio herramientas prácticas de depuración que no se aprenden solo leyendo la teoría.

## Aplicación profesional

Profundizar en esta herramienta tiene una aplicación inmediata y crítica para mí. Actualmente, dentro del equipo de desarrollo del trabajo en el que me encuentro, estoy asumiendo la responsabilidad de estructurar la dockerización completa de nuestro proyecto principal (abarcando el *backend* completo, bases de datos como PostgreSQL y demás servicios).

## Próximos pasos

Entender a este nivel de detalle cómo inspeccionar contenedores, gestionar sus puertos y entrar a sus sistemas de archivos para configurarlos desde adentro me da la base arquitectónica necesaria para dejar de lado las configuraciones manuales y pasar a despliegues mucho más robustos, escalables y estandarizados para todo el equipo.