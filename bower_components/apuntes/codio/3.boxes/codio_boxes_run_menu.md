## Crear botón de reinicio Apache-MySQL.
1. Crea un nuevo archivo llamado `reinicar.sh` en la raiz del proyecto y pega esto:

		#!/bin/sh
        parts stop apache2 mysql
    	parts start apache2 mysql

2. En archivo `.codio` y añade el botón que ejecute `sh reinicio.sh` así:

        "commands": {
            "Node version": "node --version",
            "Reinicar Apache-mysql": "sh reinicio.sh"
        },

	Ya tenemos un botón para reiniciar rápidametente en el Run-Menú

	![](https://raw.githubusercontent.com/zapcode/apuntes/master/codio/img/reiniciar.sh-apache-mysql-codio.gif)

## Crear botón de guardado GIT remoto.
1. crea un archivo `guardar.sh` en la raiz con esto:

		#!/bin/sh
		git add --all
		git commit -m "guardado automático desde codio"
		git push origin master

2. En archivo `.codio` añade en `commands` el comando así:

          "commands": {
                "Node version": "node --version",
                "Reinicar Apache-mysql": "sh reinicio.sh",
                "Guardar": "sh guardar.sh"
          },

	Luce muy bien:
    
	![](https://raw.githubusercontent.com/zapcode/apuntes/master/codio/img/codeio_command_guardar.sh.png)


## RECURSOS:
<https://codio.com/s/docs/boxes/run/>