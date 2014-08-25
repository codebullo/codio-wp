
# Tar - Compresor/descompresor
## DESCOMPRIMIR CON `tar`
* Descargamos wp con `wget` para practicar:
    ```
wget http://es.wordpress.org/wordpress-3.9.2-es_ES.tar.gz
    ```
* Descomprime en directorio actual:
    ``` 
tar -xzvf wordpress-3.9.2-es_ES.tar.gz
    ```
* Descomprime en carpeta (Debe existir la carpeta o dará error):
	* Pasamos 2 comandos, 1º crea carpeta blog y 2º descomprime en ella:
    ``` 
mkdir blog | tar -xzvf wordpress-3.9.2-es_ES.tar.gz -C blog
    ```
 
 
## COMPRIMIR/EMPAQUETAR con `tar`:
    
`tar` `letras-opciones` `destino.tar` `carpeta`
   
   ```
tar cvf paquete_de_carpeta.rar carpeta
    ```
* CREAR PAQUETE CON COMPRESIÓN Gzip COMPRIMIDO `czvf `:
    ```
    tar czvf paquete_de_carpeta.tar carpeta
    ```
	* AYUDA:
    	* `tar --usage`
        * `tar --help`
        
	- OPCIONES: 
        - `x` => `xvf` Extrae tanto con/sin comprimir.
        - `v` => `vf` Verbose (Muestrar información) *recomendado*
        - `f` => File (actua en fichero) *requerido*
        - `t` => `tvf` Test, Leer sin extraer.
        
    	+ `c` => `cvf` Create (Crear paquete)
        + `cz` => `czvf` Crea comprimido con Gzip.
        + `-C` => Change directory (Destino en otra carpeta existente)

    + LAS LETRAS DESPUÉS DE `tar` PASAN OPCIONES
    	+ El orden no afecta pero se recomienda finalizar por `vf`
        - `xf` => Extrae archivo.tar.
        - `xvf` => Extrae viendo información.
        ```
        tar xvf comprimido.tar
        ```
        + `cf` => Crea/empaqueta sin mostrar info.
        + `cvf` => Crea/empaqueta con información.
        ```
        tar cvf comprimido.tar
        ```
        + `czf` => Crea/gzip comprimido
        + `czvf` => Crea/gzip comprimido mostrando info.
        
	- Ejemplos prácticos:

        + Empaqueta nombrecarpeta y sus contenidos
        	+ `tar cvf nombrecarpeta.tar nombrecarpeta`
        - Muestra contenido de paquete.tar sin descomprimirlo.
        	- `tar tvf paquete.tar`
        + Desempaquetar en la carpeta actual (crea carpeta lo mete dentro)
        	+ `tar xvf /home/jose/paquete.tar`
        - Comprimir carpeta y contenidos
        	- `tar czvf nombrecarpeta.tar.gz nombrecarpeta`
        * Desempaquetar en otra carpeta "carpeta" (debe existir)
        	* `tar xvf paquete.tar -C otracarpeta`
        + Comprobar su contenido de archivo.tar
        	+ `tar tvf archivo.tar.gz`
        - Descomprimir y desempaquetar en la carpeta actual (crear una carpeta y metelos dentro)
        	- `tar xvf /home/jose/paquete.tar.gz`
        + copia de seguridad comprimida muy simple
    		+ `tar czf /var/my-backup.tgz /home/paco/`

            
            