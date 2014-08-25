
# Projecto Wordpress en codio.com

Para esta documentación he utilizado 
<https://codio.com/zapcode/codio-wordpress>

## 0. Donde encontrar wordpress actualizado.

- En inglés el paquete con la última versión esta: 
	- <http://wordpress.org/latest.tar.gz>
- En español (en `.zip` y `.tar.gz`) multiples versiones:
	- <http://es.wordpress.org/releases/>
    - <http://wpcentral.io/internationalization/>

Podemos descargarla normalmente o hacerlo con la terminal con `wget` pulsamos sobre el enlace `botón derecho` y `copiar enlace` será algo así. 
- <http://es.wordpress.org/wordpress-3.9.2-es_ES.tar.gz>


## 1: Descarga y descompresión de wordpress

Descarga wordpress en español desde la terminal con  `wget`:

	wget http://es.wordpress.org/wordpress-3.9.2-es_ES.tar.gz

Descomprime desde la terminal con `tar`:
		
    tar -xzvf wordpress-3.9.2-es_ES.tar.gz

En el comprimido wp esta en la carpeta `wordpress` por lo que nos creará dicha carpeta en la raíz.


## 2: Instalar PHP, APACHE Y MYSQL
1. Necesitamos estos componentes instalados para ejecutar wordpress, esto instala
PHP5, Apache, MySQL y todos los otros módulos requeridos.
		
    	parts install php5 php5-apache2 php5-pdo-mysql php5-zlib mysql

2. Arranca los servicios con :

		parts start apache2 mysql




## 3: Creación de la base de datos MySQL
Ahora tenemos que conseguir una configuración de base de datos MySQL y utilizables por Wordpress

1. Accede como `root`= `Administrador` en la terminal de MySQL shell
	```
	mysql -u root -p
	```
2. Nos preguntará por la contraseña, por defecto no hay ninguna así que presiona `Enter` y deberías estar en la consola de MySQL con derecho de administración:
	```
	mysql>
	```
3. Ahora creamos la base de datos con el nombre `wordpress` así:
	```
	CREATE DATABASE wordpress;
    #Query OK, Query OK, 1 row affected (0.00 sec)  
	```
	Comprueba si existe, para ver las bases existentes escribe:
	```
	SHOW DATABASE;
	```
4. Creamos un usuario llamado `wordpressuser`con acceso al localhost:
	```
	CREATE USER wordpressuser@localhost;
    # SALIDA = Query OK, 0 rows affected (0.00 sec)
	``` 
5. Añadimos una contraseña a el usuario creado:
	```
	SET PASSWORD FOR wordpressuser@localhost= PASSWORD("password");
	# SALIDA = Query OK, 0 rows affected (0.00 sec) 
	```
6. Concedemos permisos totales al usuario para modificar la base de datos:
	```
	GRANT ALL PRIVILEGES ON wordpress.* TO wordpressuser@localhost IDENTIFIED BY 'password';
	# SALIDA = Query OK, 0 rows affected (0.00 sec) 
	```
7. Recargamos los privilegios para que tengan efecto.
	```
	FLUSH PRIVILEGES;
	# SALIDA = Query OK, 0 rows affected (0.00 sec) 
	```
8. Salimos de la consola MySQL:
	```
	exit
	```

## 4: Modificando el `wp-config-sample.php` `wp-config.php`

- Abra la carpeta wordpress y renombre `wp-config-sample.php`a `wp-config.php` y abrelo.

- Modifica y rellena con el usuario, nombre de base de datos y contraseñas:

```
define('DB_NAME', 'database_name_here');
/** MySQL database username */
define('DB_USER', 'username_here');
/** MySQL database password */
define('DB_PASSWORD', 'password_here');
```

- El resultado para este ejemplo sería este:

```
define('DB_NAME', 'wordpress');
/** MySQL database username */
define('DB_USER', 'wordpressuser');
/** MySQL database password */
define('password', '');
```

- En el `wp-config.php` añadimos 2 lineas que indican el subdominio que crea codio en box url, añadimos debajo de `<?php`.

```
define('WP_HOME','http://mailbox-spoon.codio.io:3000/wordpress');
define('WP_SITEURL','http://mailbox-spoon.codio.io:3000/wordpress');
```
NOTA: escribimos al final `/wordpress` porque no se modifico ni se movió el contenido por defecto, si deseas cambiar esta ruta, deberás añadir el nombre que de tu carpeta que contiene wordpress, si deseas que wordpress se encuentre en la raiz la url elimina /wordpress de esas dos lineas y mueve todo el contenido de /wordpress a la raiz de tu proyecto.

## 5: Arrancando la instalación de wordpress
+ Ahora deja a wordpress installer hacer el resto.
	1. En el Preview menu, selecciona `Box URL`
	2. añade en la URL al final `/wordpress/wp-login.php` en mi caso así:
```
	http://mailbox-spoon.codio.io:3000/wordpress/wp-login.php
```
3. Realizar la instalación.
    * Escribe el título del sitio.
    * Escribe un nombre de usuario.
    * Una contraseña.
    * Un correo electrónico.
    * EN `Privacy: Allow search engines to index this site`.
	* Activalo: Permitirás que google indexe el blog.
    * Desmarcado: El blog no será indexado.
        * Nota: Podrá modificar esta configuración en `Configuración` -> `Lectura`

- Para trabajar mejor en el puerto 3000 Instala un Wordpress Plugin.
1. Ve a plugins.
2. Busca por `permalink-fix-disable-canonical-redirects-pack` y instalalo.
3. Activa el Plugin.


## Cambiando idioma de instalación en inglés.
1. Descarga wp en español y descomprimelo en carpeta:
```
mkdir wp-es | tar -xzvf wordpress-3.9.2-es_ES.tar.gz -C wp-es
```
2. Abre `wp-es`, entra en `wp-content` y mueve la carpeta `languages` a la carpeta `wp-content` del wordpress que esta en inglés.


3. Abre el archivo `wp-config.php` de tu wp en inglés y módifica la linea:
```
	define('WPLANG', '');
```
	así:
```
define('WPLANG', 'es_ES');
```

## DESPLIEGUE E INTEGRIDAD DE LA DB

PENDIENTE

Enlaces de interes:

- <http://crowdfavorite.com/ramp/>
- <http://wordpress.org/plugins/duplicator/>
- <http://www.chefduweb.nl/2013/10/deploying-wordpress-part-3/>
- <https://deliciousbrains.com/wp-migrate-db-pro/>
- <https://www.digitalocean.com/community/tutorials/how-to-use-rsync-to-sync-local-and-remote-directories-on-a-vps>

## Fuentes:

- <https://codio.com/s/docs/specifics/wordpress/>
- <http://www.vozidea.com/como-instalar-wordpress-desde-la-consola-ssh>
- <http://codex.wordpress.org/Installing_WordPress_in_Your_Language>
- <http://codex.wordpress.org/Installing_WordPress>
- <http://codex.wordpress.org/Translating_WordPress>

## AYUDA

IRC WORDPRESS