

## Entorno de los proyectos

#### Tenemos disponible:

### En las boxes de codio viene preinstalado:

- rbenv ¿Es para intercambiar entre versiones ruby?

- NodeJS Bajo NVM
	- Fuente: <https://codio.com/s/docs/specifics/node/>
	- Ayuda:
    ```
    nvm help
    ```
	- Node Version Manager - Una librería que gestiona multiples versiones intercambiables)
	- 
    ```
    node --version
    #v.0.10.25
    ```
    - Para instalar una versión diferente de Node:
    - 
    ```
    nvm install 0.8
    # Instala versión 0.8.26
    ```
    - Mostrar versiones disponibles:
    ```
    nvm ls
    ```
    - Ahora cambio facil entre versiones:
    ```
    nvm use 0.10 # usar la 0.10
    nvm use 0.8 # usar la 0.8
    ```

- ### Parts
- #### Fuente: <https://codio.com/s/docs/boxes/box-parts/>
	- `parts install PACKAGE`
    	- Install one or many packages.
    + `parts uninstall PACKAGE`
    	+ Uninstall one or many packages.
    - `parts upgrade PACKAGE`
    	- Actualizar uno o muchos paquetes.
    + `parts purge PACKAGE`
    	+ Uninstall and remove leftover data of one or many.
    - `parts list`
    	- Lista todos los paquetes instalados.
    + `parts serch TERMINO`
    	+ Busca paquetes con TERMINO
    - `parts start PACKAGE`
    	- Start one or many services of packages.
    + `parts stop PACKAGE`
    	+ Stop one or many servicies of packages.
    - `parts restart PACKAGE`
    	- Restart one or many services.
    + `parts status PACKAGE`
    	+ Show status of one.
    - `parts update PACKAGE`
    	- Update Box Parts.
    + `parts info PACKAGE`
    	+ Show dependencies.
    - `parts env`
    	- Muestra los comandos.
        
- ### PARTS: Configuración de entornos.

- #### PHP
	- 
    
- ### Yo
- ### Grunt - see <http://gruntjs.com/>
	- `npm install -g grunt-cli`
    	- Instala console line interface "grunt-cli"
        
    + `grunt`
    	+ Arrancar grunt
    
    - `grunt --help`
    	- Mostrar ayuda
    
    + `grunt [options] [task [task]]`
    	+ Uso.
    
    * #### Opciones grunt-cli:
    
    	- `--help`, `-h`
        	- Mostrar ayuda.
            
        + `--base`
        	+ Specify an alternate base path. By default, all file paths are relative to the Gruntfile. (grunt.file.setBase).
        
        - `--no-color`
        	- Disable colored output. 
            
        + `--gruntfile`
        	+ Specify an alternate Gruntfile. By default, grunt looks in the current or parent directories for the nearest Gruntfile.js or Gruntfile.coffee file.
            
        - `--debug`, `-d`
        	- Enable debugging mode for tasks that support it.
            
        + `--stack`
        	+ Print a stack trace when exiting with a warning or fatal error.
        
        - `--force`, `-f`
        	- A way to force your way past warnings. Want a suggestion? Don't use this option, fix your code.
        + `--tasks`
        	+ Additional directory paths to scan for task and "extra" files (grunt.loadTasks).
            
        - `--npm`
        	- Npm-installed grunt plugins to scan for task and "extra" files. (grunt.loadNpmTasks).
        
        + `--no-write`
        	+ Disable writing files (dry run).
        
        - `--verbose` , `-v`
        	- Verbose mode. A lot more information output. 
            
        + `--version`, `-V`
        	+ Print the grunt version. Combine with --verbose for more info.
            
        - `--completion`
        	- Output shell auto-completion rules. See the grunt-cli documentation for more information.
        
            
            
            
            
            
            
            


- ### Emmet

- ### NODE
	- `man node | tee nodemanual.txt`
    	- Manual node salida crearda en nodemanual.txt

- ### Bash

	+ `history`
    	+ Muestra el historial de comandos.
	- `whereis bash`
    	- Muestra donde esta instalado bash
        
    + `/bin/bash codigo.sh`
    	+ Ejecuta comandos en archivo código.sh
  
	- `which programa`
    	- indica la ruta completa de PROGRAMA, si éste está accesible a través de la variable PATH..
        	+ Ejemplos:
            	+ `which ruby` => `/home/codio/.rbenv/shims/ruby`
                + `which npm` => `/home/codio/.nvm/v0.10.25/bin/npm`
                + `which grunt` => `/home/codio/.nvm/v0.10.25/bin/grunt`
                + `which yo` => `/home/codio/.nvm/v0.10.25/bin/yo `
                
    + `comando | tee archivo.txt`
    	+ Escribe salida en archivo.txt
        
    - #### AYUDA:
    + `man programa`
    	+ Muestra manual de la aplicación.
        
    - `man /bin/bash | tee bashmanual.txt`
    	- Manual de bash salida crearla en bashmanual.txt`
    
    + `man -K palabra`
    	+ Busca en el manual la palabra.
        
    - `man -f comando`
    	- Detalles asociados a este comando.
        
    + `info programa`
    	+ Mas información de un particular comando.
        
    - `-?`, `--h`, `--help`, `-h`
    	- Otros alias que pueden mostrar ayudas.
        
    + `aplicación --help`
    	+ Muestra mensaje de uso de la aplicación.
        
    - `--help | tee archivo.txt
    	- Guarda ayuda en archivo.txt
    

- ### git

- ### unzip
	- `unzip file.zip`
    	- Descomprime file.zip en ruta actual.
	- `unzip file.zip -d carpetadestino`
    	- Descomprime file.zip en carpetadestino
    + AYUDA: `unzip --help`
- ### wget
	- `wget http://www.web.com/loquesea.zip`
    	- Descarga archivo
    + `wget -c` continua la descarga donde lo deja.
    + `wget -b` continua aun si salimos terminal
    
    - `wget -p`
    	- descargar todos los archivos que son necesarios para mostrar correctamente una determinada página HTML, incluyendo imágenes.
        
    + `wget --random-wait`
    	+ espera un tiempo aleatorio entre descarga, para evitar entrar en la lista de negra.
        
    - `--limit-rate=200k`
    	- Limita la velocidad a la que descarga a 200k.
- ## npm 
    - USO: `npm COMANDO`
    - Donde COMANDO puede ser:
    
        ```
        add-user, adduser, apihelp, author, bin, bugs, c, cache,
        completion, config, ddp, dedupe, deprecate, docs, edit,
        explore, faq, find, find-dupes, get, help, help-search,
        home, i, info, init, install, isntall, issues, la, link,
        list, ll, ln, login, ls, outdated, owner, pack, prefix,
        prune, publish, r, rb, rebuild, remove, repo, restart, rm,
        root, run-script, s, se, search, set, show, shrinkwrap,
        star, stars, start, stop, submodule, tag, test, tst, un,
        uninstall, unlink, unpublish, unstar, up, update, v,
        version, view, whoami 
        ```
	- `npm -v`
    	- Muestra version instalada.
    + `npm help TERMINO`
    	+ Busca en la ayuda TERMINO
    * `npm init`
    	* Crea/modifica/genera un package.json
        
    - `npm search "textoabuscar"`
    	- Busca paquetes con "texto a buscar".
        
    + `npm info nombre-del-modulo`
    	+ Muestra información del paquete.
        
    - #### npm install:
    	- npm install
        - npm install pkg
        - npm install pkg@tag
        - npm install pkg@version
        - npm install pkg@version range
        - npm install folder
        - npm install tarball file
        - npm install tarball url
        - npm install git:// url
        - npm install github username/github project
    * #### NPM AYUDA: 
        * `npm help npm`
    		* Ayuda de npm.
        + `npm faq`
            + Preguntas y respuestas frecuentes
        * `npm faq | tee npmfaq.txt`
    		* Guarda en npmfaq.txt salida de "npm faq"
        - `npm -h`
    		- Muestra ayuda npm
	    * `npm COMANDO -h`
			* Muestra ayuda del comando
        - `npm -l`
        	* Muestra ayuda de uso completa.
            
            
            
            
- node

- grunt

- #### bower
    - Instalar
    	- ### `bower install`
    - Buscar
    	- ### `bower search`
        

- ruby
	- Ruby 2.0.0p353
- python27
- ### grep
	- USO: 
    - USO2: `grep palabra`
    	- Busca `palabra` en ruta actual.
    - AYUDA: `grep --help`
- ### curl
- ### gem  `2.0.14`
	+ All info: [rubygems.org-command-reference](http://guides.rubygems.org/command-reference/)
    
    + Gem build:
    	+ Build a gem from a gemspec
    	+ ### `gem build GEMSPEC_FILE "options"`
        
        	- Options:
            	- `--force` skip validation of the spec.
            - Common Options:
            	- `-h, --help`- Get help on this command.
                - `-V, -[no-]verbose`- Set the verbose level of output
                - `-q, --quiet`- Silence commands.
                - `--config-file FILE`- Usage this config file instead of default.
                - `--backtrace`- Show stack backtrace on errors.
                - `--debug`- Turn on Ruby debugging.


#### Esta desactivado:

- apt-get
- bash


Fuentes: 

<http://www.gnu.org/software/coreutils/manual/coreutils.html>
