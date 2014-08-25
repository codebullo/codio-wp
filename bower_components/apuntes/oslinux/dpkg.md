- ### dpkg 
    + `dpkg --get-selections`
    	+ Muestra todos los instalados.
        
    * `dpkg --get-selections | tee paquetes.txt`
    	* Lista de paquetes instalado en paquetes.txt
        
    - `dpkg --get-selections | grep php` 
    	- Muestra instalados con la php.
      
    + `dpkg --get-selections > mis_paquetes`
    	+ Exporta lista de paquetes instalados.
        
    - `dpkg --set-selections < mis_paquetes`
    	- Obtención de la lista de paquetes.
        
    + `apt-get dselect-upgrade`
    	- Instalación de la lista.
        
    - `-e robots=off`
    	- no descargar el archivo robots.txt
    
    + AYUDA: `dpkg --help`
    

