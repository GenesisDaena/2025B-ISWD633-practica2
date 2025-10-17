# Variables de Entorno
### ¿Qué son las variables de entorno?
# COMPLETAR
Son pares nombre=valor que el sistema y los programas pueden leer para saber configuraciones importantes y saber cómo comportarse o dónde encontrar ciertas cosas

### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

# COMPLETAR
docker run -d --name mi_nginx -e username=daena -e role=admin nginx:alpine

# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR
<img width="855" height="232" alt="image" src="https://github.com/user-attachments/assets/071447fb-c9d1-4e73-8bfc-5c8bc181c65c" />



### Crear un contenedor con la imagen de mysql, mapear todos los puertos
# COMPLETAR
```
docker run -d --name mi_mysql -P mysql:8.0
```


### ¿El contenedor se está ejecutando?
# COMPLETAR
<img width="1249" height="67" alt="image" src="https://github.com/user-attachments/assets/66936593-c2c3-4ea1-8350-ff84258783fc" />


### Identificar el problema
# COMPLETAR
<img width="928" height="151" alt="image" src="https://github.com/user-attachments/assets/b05951d1-add5-4fa3-b3b8-41a104e32ee5" />

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

### ¿Qué bases de datos existen en el contenedor creado?
# COMPLETAR
<img width="1083" height="259" alt="image" src="https://github.com/user-attachments/assets/614f4d87-897c-44ae-a26e-40c300112463" />


