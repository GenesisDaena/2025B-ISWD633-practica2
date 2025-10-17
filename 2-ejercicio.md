### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:15-alpine3.21
# COMPLETAR
docker run -d --name postgresdb -e POSTGRES_PASSWORD=12345 postgres:15-alpine3.21

### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4
docker run -d --name cliente_pg -e PGADMIN_DEFAULT_EMAIL=admin@example.com -e PGADMIN_DEFAULT_PASSWORD=admin123 -p 5050:80 dpage/pgadmin4


# COMPLETAR

La figura presenta el esquema creado en donde los puertos son:
- a: 5050
- b: 80
- c: 5432

![Imagen](esquema-2-ejercicio.PNG)

## Desde el cliente

### Acceder desde el cliente al servidor postgres creado.
# COMPLETAR CON UNA CAPTURA DEL LOGIN
<img width="1232" height="715" alt="image" src="https://github.com/user-attachments/assets/b9327733-3b95-4722-b15c-0080a375f625" />

### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.

## Desde el servidor postgresl
### Acceder al servidor
```
docker exec -it postgresdb psql -U postgres
```

### Conectarse a la base de datos info
# COMPLETAR
```
 \c info
```

### Realizar un select *from personas
# AGREGAR UNA CAPTURA DE PANTALLA DEL RESULTADO
<img width="250" height="105" alt="image" src="https://github.com/user-attachments/assets/245f768f-33d5-4e26-9a0a-5ffc60ab2186" />

