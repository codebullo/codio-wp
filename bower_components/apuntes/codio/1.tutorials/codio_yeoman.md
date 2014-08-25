
## YEOMAN, Grunt, Bower and Yo in Codio
### Basado de `tutorial_yo_agular` que funciona dentro de codio...

Objetivos tareas a aprender:

- Unussed css
- soucemap : grunt-concat-sourcemap o alternativa
- practicar a crear generadores con tareas personalizadas crear manuales.

Codio recibe el apoyo de Addy Osmany, que es colaborador de yeoman, por lo tanto no es de estrañar que se incluya documentación y soporte para dicha herramienta.

Para prueba vamos a comenzar instalando las herramientas que necesitamos en la terminal 
de nuestra codio box.


## CREANDO PROYECTO ASOCIADO A GIT REMOTO: 

- Creamos un repositorio nuevo en github/bitbucket
- En codio pulsaoms en `Create Proyect` y seleccionamos `GIT`
- Pegamos el url del git y pulsamos `Create` y ya esta.

## Configura LIVERELOAD en Gruntfile.js para codio.com

funcionan los puertos 1024 a 9999 sobre la `linea 60` cambiaremos esto:

    // Change this to '0.0.0.0' to access the server from outside.
    hostname: 'localhost',
    livereload: 35729

Por esto otro:

    // Change this to '0.0.0.0' to access the server from outside.
    hostname: '0.0.0.0',
    livereload: 4000  
    
## 1 - Instala global Yeoman (yo, bower y grunt).

	npm install -g yo

opcional: comprobar si se instalo:

	yo --version && bower --version && grunt --version
    
para actulalizar: 
	
    npm udpate -g yo

## 2 - Instala global `grunt-cli`:

	npm install -g grunt-cli

Arrancar el asistente de `yo`

	yo
    
    
# INSTALANDO Y CONFIGURACIONES GENERADORES
## 3A - Instalar generator-angular

- `nmp install generator-angular`
   - Requiere:
   - NOTA: Podemos ver lista de gem instalada con `gem list`
   		`gem install sass compass`
        
        

Para ejecutar yo simplemente ponemos:

yo

- MENÚ de yeoman:
	+ `ARRIBA` Y `ABAJO` => DESPLAZARSE 
	+ `ENTER`  => ACEPTAR OPCIÓN
	+ `ESPACIO` => SELECCION OPCIONES VARIAS

Escribimos para buscar en generadores y pulsamos `ENTER`, una vez instalado damos `Run the xxxxxx generator`. También podemos directamente escribir en la consola `yo nombre-generator`

Ahora necesitamos con bower que nos meterá en `bower_components` lo listado en el `bower.json`:

	bower install

Si vamos a trabajar con SASS con compilador de Ruby y no `libsass` de nodejs, tendremos que instalar sass que nos pide el módulo grunt-contrib-sass, sinó nos dará error el la tarea sass `sass task`
- más info: <https://github.com/gruntjs/grunt-contrib-sass>

Instalamos Sass con Gems:
```
gem install sass
```
Ahora ya podemos crear todas las tareas de `grunt` escribimos:
```
grunt build
```



sobre la `linea 53` cambiamos esto:
- 
Por esto otro NOTA ME DIO FALLO CON WEBAPP, ESTO NO CAMBIARLO EN ESE GENERADOR

    files: [
          '<%= yeoman.app %>/{,*/}*.html',
          '.tmp/styles/{,*/}*.css',
          '<%= yeoman.app %>/images/{,*/}*.{png,jpg,jpeg,gif,webp,svg}'
        ]


    files: [
          '<%= yeoman.app %>/{,*/}*.html',
          '<%= yeoman.app %>/scripts/{,*/}*.js',
          '.tmp/styles/{,*/}*.css',
          '<%= yeoman.app %>/images/{,*/}*.{png,jpg,jpeg,gif,webp,svg}'
        ]

## PREPARACIÓN PARA generator-wordpress 

* https://github.com/wesleytodd/YeoPress

Instalamos el generador si no lo tenemos:

	npm install -g generator-wordpress

Arrancamos el generador así: 

	yo wordpress


## DIFERENCIAS EN GENERATOR-WEBAPP-PHP

Necesitará que instales:

Compass:

	gem install compass

Apache:

	parts install php5 php5-apache2

Reinicio apache:

	parts restart apache2

## CONFIGURACIÓN DE CODIO MENUS

Codio tiene la capacidad de ahorrar un montón de tiempo mediante la configuración del menú "Ejecutar" (comandos de la CLI) y del menú 'Vista previa'. 

Haga clic en `Configuration...` esto nos creará/abrirá automáticamente el archivo `.codio`.

![](https://raw.githubusercontent.com/zapcode/apuntes/master/codio/img/codio_run_preview_menu.png)

Por defecto contendrá esto:

    {
    // Configure your Run and Preview buttons here.

    // Run button configuration
      "commands": {
            "Node version": "node --version"
      },

    // Preview button configuration
      "preview": {
            "Project Index (static)": "https://{{domain}}/{{index}}",
            "Current File (static)": "https://{{domain}}/{{filepath}}",
            "Box URL": "http://{{domain}}:3000/",
            "Box URL SSL": "https://{{domain}}:9500/"
      }
    }

Vamos a cambiarlo por esto otro:

    {
    // Configure your Run and Preview buttons here.

    // Run button configuration
      "commands": {
        "Grunt Serve": "grunt serve",
        "Grunt Test": "grunt test",
        "Grunt Build": "grunt",
        "Grunt Serve:Dist": "grunt serve:dist"
      },

    // Preview button configuration
      "preview": {
        "Yeoman Demo": "http://{{domain}}:9000/"
      }
    }

Como vés los botones de `run` ahora ejecutan los comandos que hemos configurado, estupendo...

Arrancamos el servidor con el botón o escribimos:

	grunt serve

Pulsamos en boton Preview que hemos configurado `Yeoman Demo`

