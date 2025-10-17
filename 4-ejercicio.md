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
docker run -d --name mysql --network net-wp -e MYSQL_ROOT_PASSWORD=root123 mysql:8
``` 

### Crear el contenedor wordpress a partir de la imagen: wordpress, configurar las variables de entorno necesarias
# COMPLETAR
```
docker run -d --name wordpress --network net-wp -e WORDPRESS_DB_HOST=mysql:3306 -e WORDPRESS_DB_USER=root -e WORDPRESS_DB_PASSWORD=root123 -e WORDPRESS_DB_NAME=wordpress -p 9300:80 wordpress
```

De acuerdo con el trabajo realizado, en el esquema del ejercicio el puerto a es **9300**

Ingresar desde el navegador al wordpress y finalizar la configuración de instalación.
# COLOCAR UNA CAPTURA DE LA CONFIGURACIÓN
<img width="1017" height="975" alt="image" src="https://github.com/user-attachments/assets/81923c22-3518-4920-baaf-c069df2ca4e7" />

<img width="1112" height="542" alt="image" src="https://github.com/user-attachments/assets/4b9b0923-6ca8-4f24-a003-45a29c979712" />


Desde el panel de admin: cambiar el tema y crear una nueva publicación.
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress
# COLOCAR UNA CAPTURA DEL SITO EN DONDE SEA VISIBLE LA PUBLICACIÓN.
<img width="1230" height="1025" alt="image" src="https://github.com/user-attachments/assets/b6269dd4-e34a-4263-93da-a62e252ba762" />

<img width="1246" height="1029" alt="image" src="https://github.com/user-attachments/assets/0071c3ec-6172-4db3-a56e-b2cbff7f049f" />

### Eliminar el contenedor wordpress
# COMPLETAR
docker rm -f wordpress

### Crear nuevamente el contenedor wordpress
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress

### ¿Qué ha sucedido, qué puede observar?
# COMPLETAR
Al volver a crear el contenedor WordPress, el sitio web y las publicaciones se mantienen igual que antes. Esto ocurre porque la información de entradas, temas o usuarios está almacenada en la base de datos MySQL, no dentro del contenedor de WordPress. Por tanto, aunque el contenedor WordPress se elimine y vuelva a crearse, el contenido persiste gracias a que el contenedor mysql sigue activo y con los mismos datos.

