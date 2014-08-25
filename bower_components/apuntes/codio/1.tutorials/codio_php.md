# PUESTA EN MARCHA: 

1_ En la terminal, INSTALAR PHP Y APACHE 2. Comprueba si ya lo tienes con `parts list`

- AYUDA 
	
   
    parts --help 

Comprobar el estado de los servicios de `parts` :

	parts status apache2
    #apache2 STOPPED // El servidor esta detenido
    #Started: apache2 //El servidor esta encendido

Instala todo asi

	parts install php5 php5-apache2
 

2_ ARRANCA PHP-APACHE: para pararlo: `parts stop apache2` y reinicio `parts restart apache2`
```
parts start apache2
```

3_ EN PESTAÑA PREVISUALIZAR MARCA `BOX URL SSL` Y:
	* `Inside Codio tab` => para previsualizar en Codio.
    * `New Brower Tab` => para previsualizar en navegador.


_YA PUEDES CODEAR PHP EN CODIO Y PREVISUALIZAR_

# EDITAR ARCHIVOS APACHE-PHP Especiales:

### php.ini, Archivo de configuración de php
```
nano /home/codio/.parts/etc/php5/php.ini
```
### httpd.conf, Archivo de configuración de apache
```
nano /home/codio/.parts/etc/apache2/httpd.conf
```

# VERSION + DETALLADA A CONTINUACIÓN....

PHP no está preinstalado en Cajas Codio pero es muy fácil de instalar. Actualmente ofrecemos PHP5 pero también se puede instalar [PHPBrew](https://codio.com/s/docs/specifics/php-brew) para gestión de versiones de PHP si es necesario. He aquí cómo instalar PHP5 en su caja Codio. Se tarda 10 segundos.

### ESPAÑOL

1. Crear un nuevo proyecto.

2. Una vez que estás en el IDE, seleccione el elemento de menú "Herramientas> Terminal" para abrir una ventana de terminal.

3. Instale con paquetes `parts install php5 php5-apache2` en la línea de comandos (php5-apache incluye módulos para PHP requiere y también instala apache2, apr_util aprm y libmcrypt y módulos estándar de PHP)

```
parts install php5 php5-apache2
```

    
    ============ php5 ============                                                                                         
    PHP config file is located at:                                                                                         
    $ /home/codio/.parts/etc/php5/php.ini                                                                                

    Close and open a terminal or reload shell to                                                                           
    have installed pear packages available without full path                                                               
    $ . ./bash_profile                                                                                                     

    ============ apache2 ============                                                                                      
    To start the Apache server:                                                                                            
    $ parts start apache2                                                                                                

    To stop the Apache server:                                                                                             
    $ parts stop apache2                                                                                                 

    Apache config is located at:                                                                                           
    $ /home/codio/.parts/etc/apache2/httpd.conf                                                                          

    Default document root is located at:                                                                                   
    $ /home/codio/workspace                                                                                              
    ============ php5-apache2 ============                                                                                 
    PHP config file is located at:                                                                                         
    $ /home/codio/.parts/etc/php5/php.ini                                                                                

    If Apache2 httpd is already running, you will need to restart it:                                                      
    $ parts restart apache2 


Ahora si escribimos:

	parts list
Nos mostrará instalado:
```
libmcrypt (2.5.8)                                                       
php5 (5.5.15)                                                           
apr (1.5.1)                                                             
apr_util (1.5.3)                                                        
apache2 (2.4.9)                                                         
php5-apache2 (5.5.15)  
```

4. También puede instalar muchos módulos más de PHP y otros componentes más info=> [box parts](https://codio.com/s/docs/boxes/box-parts).

5. PHP está instalado y listo para usar.

6. Escriba `parts start apache2` para iniciar servidor Apache.

* Detener con  `parts stop apache2`
* Reiniciar con `parts restart apache2`

### Acceso a su aplicación

Una vez que su aplicación PHP es en servicio, puede acceder a su proyecto desde un navegador o API llamada etc

#### Previsualizar:

1 - Arranque APACHE2

	parts start apache2
    
- Nos dará
```
=> Starting apache2...                                                  
=> Started: apache2  
```
* Para comprobar si esta arrancado
	```
	parts status apache2
    #apache2 STOPPED  
    ```

2 - Abra Box Url Preview con `Box URL SSL` y `Inside Codio` para verlo dentro de codio o `New Browser Tab` para previsualizar en nueva pestaña del navegador.

![](https://raw.githubusercontent.com/zapcode/apuntes/master/codio/img/php_preview_box_url.png)

Puede acceder a su proyecto de PHP desde el menú de vista previa Codio (la más opción del menú Codio derecha). Seleccione el menú desplegable del menú y luego seleccione 'Caja URL' que accede en Puerto 3000. O puede usar 'Recuadro URL SSL "que accede a ella en el puerto 9500 a través de HTTPS.
