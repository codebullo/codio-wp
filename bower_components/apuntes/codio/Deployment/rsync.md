

# rsync

Es recomendable tener `GIT` del proyecto en estado anterior para revertir cambios

## Configurar Plesk para acceso SSH
Si tenemos Plesk seleccionamos así:

Usamos el usuario y pass de FTP.

Debemos dar permiso de acceso SSH en plesk vamos a:

`Suscripciones` -> `Sitios web y dominios` -> `Acceso FTP`.

Elegimos usuario y en `Acceder al servidor vía SSH` seleccionamos `/bin/bash` y `Aceptar`

## CONEXIÓN SSH

Conectamos así y ponemos el PASS:

	ssh usuario@IP
    
Tambien podemos entrar por el dominio:

	ssh usuario@dominio.com

Para ver directorios escribimos:

	ls

Nos saldra algo asi:

	error_docs  etc  httpdocs  logs

httpdocs es el directorio de nuestro dominio principal entramos:

	cd httpdocs

Si queremos subir a el dominio principal el proyecto escribimos
para saber la ruta completa `Path`.

	pwd

Sera algo así como esto:

	/var/www/vhosts/dominio.com/httpdocs/

si queremos subirlo alguna carpeta o dominio secundario sería:

	/var/www/vhost/soloaplicaciones.com/httpdocs/apuntes

## CODIO TOOLS DEPLOYMENT MANAGE TARGETS

Vamos a `Tools` -> `Deployment` -> `Manage Targets`

Lo rellenamos así:

![](https://raw.githubusercontent.com/zapcode/apuntes/master/codio/img/codio_rsync.png)

En `Hostname`: podemos poner la IP o el dominio central `soloaplicaciones.com` por ejemplo.

EN `Destination path`: si no existe la carpeta indicada la creará.

Es conveniente enviár a un directorio y mover su contenido por ssh si no estamos
seguros.

`Delete missing directories` Activado: Borrará archivos eliminados.