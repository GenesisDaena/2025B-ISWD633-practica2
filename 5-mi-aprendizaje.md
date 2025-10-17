# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado al realizar la práctica también se debe documentar.

Al comienzo de la práctica comprendía regularmente lo que signficaban las variables de entorno, pero ahora entiendo mejor su importancia y cómo usarlas en Docker. También, aprendí que las variables de entorno sirven para configurar los contenedores sin tener que modificar el código, y que también se pueden usar para manejar información sensible como contraseñas o claves. Además, comprendí que los contenedores se conectan por defecto a una red de tipo bridge y que se pueden crear redes personalizadas para que se comuniquen entre sí. Durante la práctica también vi cómo crear contenedores con diferentes imágenes y cómo conectarlos entre ellos por medio de una red  y esto me ayudó a entender un poco cómo funcionan las aplicaciones compuestas por varios servicios.


# Consultar: Cómo se gestionan datos confidenciales con los secretos de Docker (Docker Secrets).

Los datos confidenciales se gestionan con Docker Secrets almacenándolos de forma cifrada dentro del clúster y entregándolos solo a los contenedores autorizados como archivos temporales en /run/secrets/, evitando exponerlos en el código o en variables de entorno. Docker los mantiene protegidos en memoria y nunca los guarda en texto plano dentro de la imagen ni del disco. Cuando el contenedor o servicio se elimina, el secreto también se borra automáticamente, garantizando su seguridad.

