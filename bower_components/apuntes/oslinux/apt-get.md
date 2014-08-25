

## Comando apt-get en Ubuntu

### Actualizado a 20 de Abril de 2014

Siguiendo mi intención de acercar la terminal (esa cosa tan rara) a los nuevos usuarios, vamos a hablar del comando "apt-get".

apt-get es la herramienta que utiliza Debian y sus derivadas (Ubuntu incluida), para gestionar los paquetes instalables disponibles en los repositorios y aunque tenemos a nuestra disposición herramientas gráficas que nos facilitan las cosas, nunca está de más saber lo que podemos hacer con apt-get desde una terminal:



En Ubuntu, los comandos administrativos, como "apt-get", deben de ser ejecutados como superusuario, anteponiendo "sudo".


Uso:

    sudo apt-get [opciones] orden [paquetes]

Ejemplos:

    sudo apt-get [opciones] install paquete1 paqquete2 ...
    sudo apt-get [opciones] remove paquete1 [paqquete2 ...
    sudo apt-get [opciones] source paquete1 paquete2 ...

[opciones] se puede utilizar o no (ver el apartado correspondiente).


Comandos "apt-get":

* Actualizar el listado de paquetes disponibles:


	sudo apt-get update


* Comprobar que todo ha ido bien tras la utilización de apt-get update:


	sudo apt-get check

* Instalar los programas deseados:


	sudo apt-get install paquete


* Reinstalar un programa:


	sudo apt-get -reinstall install paquete
    
* Actualizar solo los paquetes ya instalados que no necesitan, como dependencia, la instalación o desinstalación de otros paquetes:


	sudo apt-get upgrade

6. Actualizar todos los paquetes del sistema, instalando o desinstalando los paquetes que sean necesarios para resolver las dependencias que pueda generar la actualización de algún paquete:


	sudo apt-get dist-upgrade



* Desinstalar un paquete:


	sudo apt-get remove paquete


* Desinstalar un paquete y elimina los archivos de configuración:


	sudo apt-get remove --purge paquete
    

* Resolver problemas con dependencias y paquetes rotos:


	sudo apt-get -f install


Puede ser necesario reconfigurar dpkg con:


	sudo sudo dpkg --configure -a


* Para limpiar los paquetes descargados e instalados:


	sudo apt-get clean


* Para limpiar los paquetes viejos que ya no se usan:


	sudo apt-get autoclean


* Para buscar un paquete determinado:


	sudo apt-cache search paquete


* Descargar archivos fuente:


	sudo apt-get source paquete


* Configurar las dependencias de construcción para paquetes fuente:


	sudo apt-get build-dep paquete


* Seguir las selecciones de dselect:


	sudo apt-get dselect-upgrade


* Para conocer que paquetes hay instalados:


	sudo apt-show-versions (-u)


* Obtener más información de un paquete específico:


	sudo apt-cache show paquete


* Más información aún:


	sudo apt-cache showpkg paquete


* Para saber de que paquete depende:


	sudo apt-cache depends paquete

* Para encontrar el nombre de un paquete desde un archivo:


	sudo apt-file search archivo


* Listar el contenido de un paquete:


	sudo apt-file list paquete


* Para mantener al día esta función:


	sudo apt-file update


* Para mantener el sistema limpio de bibliotecas inútiles:


	sudo apt-get autoremove


* Actualizar la caché de paquetes (/var/cache/apt/pkgcache.bin), crea un nuevo árbol de dependencias:


	sudo apt-get check


* Mostrar un resumen de las dependencias no satisfechas en la caché de paquetes:


	sudo apt-cache unmet


* Mostrar una lista de todo lo que tenemos instalado en el sistema:


	sudo apt-cache pkgnames -generate

  
  OPT:| DETALLE
  -------- | --------
 +s | Simula una acción.
 +d | Sólo descarga.
 -y | No pregunta y asume que si a todo.
 -u | Muestra paquetes actualizados.
 -h | Muestra texto de ayuda.
 +q | Salida registrable - sin indicador de progreso.
 -qq| Sin salida, excepto si hay errores.
 -f | Intenta continuar sí la comprobación de integridad falla (dependencias rotas).
 -m | Intenta continuar si los archivos no son localizables.
 -b | Construye el paquete fuente después de obtenerlo.
 -V | Muesta números de versión detallados.
 -c=? Lee este archivo de configuración.
 -o=? Establece una opción de configuración arbitraria.


# Comando "apt":

Actualización: A partir de Ubuntu 14.04, el gestor de paquetes apt ("Avanced Package Tool") tiene nuevas opciones. Ya no es necesario escribir "apt-get" y se puede utilizar simplemente "apt", (apt seguirá funcionando).


* Buscar y mostrar los paquetes instalados por su nombre:


	sudo apt list

* Buscar en las descripciones de los paquetes:

	
    sudo apt search ...

* Mostrar los detalles de un paquete:


	sudo apt show paquete

* Actualizar la lista de paquetes disponibles:


	sudo apt update

* Instalar un paquetes


    sudo apt install paquete

Eliminar un paquete

	sudo apt remove paquete

* Actualizar el sistema actualizando paquetes


	sudo apt upgrade

* Actualizar todo el sistema eliminando, instalando o actualizando paquetes


	sudo apt full-upgrade

* Editar la información de las fuentes de software ("sources.list") llamando a nano o vim.


	sudo apt edit-sources




## FUENTES:

<http://www.ubuntu-guia.com/2011/01/comando-apt-get-en-ubuntu.html>