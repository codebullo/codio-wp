
# GUIA CURL

* SINTAXIS
	```
    curl [options] [URL]
    ```

Es una herramienta para transferir datos desde o hacia un servidor, usando uno de los protocolos soportados (DICT, FILE, FTP, FTPS, Gopher, HTTP, HTTPS, IMAP, IMAPS, LDAP, LDAPS, POP3, POP3S, RTMP, RTSP, SCP, SFTP, SMTP, SMTPS, TELNET y TFTP). El comando está diseñado para funcionar sin interacción del usuario.

Curl ofrece muchos trucos útiles, como soporte de proxy, la autenticación de usuarios, carga FTP, HTTP POST, las conexiones SSL, cookies, transferencia de archivos currículum, Metalink, y más. Como se verá a continuación, el número de características hará que su cabeza gire!

Curl es impulsado por libcurl para todas las funciones relacionadas con la transferencia-. Ver libcurl para más detalles.

normalmente muestra una barra de progreso durante las operaciones, lo que indica la cantidad de datos transferidos, la velocidad de transferencia y el tiempo estimado que queda, etc

pantallas enrollamiento estos datos a la terminal por defecto, así que si usted invoca rizo que hacer una operación y que está a punto de escribir datos en el terminal, se desactiva el indicador de progreso so pena de estropear la salida de mezcla de datos Contador de avance y respuesta.

Si quieres una barra de progreso para HTTP POST o PUT peticiones, tiene que redirigir la salida a un archivo de respuesta, utilizando redirección shell (>), -o [archivo] o similar.

No es el mismo caso para FTP upload como esa operación no escupa cualquier dato de respuesta a la terminal.

Si usted prefiere un progreso "bar" en lugar de la métrica regular, - # es su amigo.

### OPCIONES

Opciones comienzan con uno o dos guiones. Muchas de las opciones requieren un valor adicional al lado de ellos.

La forma corta "de un solo guión" de las opciones, -d por ejemplo, se puede utilizar con o sin un espacio entre ella y su valor, aunque un espacio es un separador recomendado. La forma larga "doble guión", --Hojas por ejemplo, requiere un espacio entre ella y su valor.

Corto opciones de versión que no necesitan valores adicionales pueden ser utilizados de inmediato junto a la otra, como por ejemplo, usted puede especificar todas las opciones -ô, L y -v a la vez como -OLv.

En general, todas las opciones booleanas están habilitadas con - opción y aún inhabilitadas nuevo con - no- opción. Es decir, se utiliza el mismo nombre de la opción exacta pero añadiendo al principio de "no". Sin embargo, en esta lista que en su mayoría sólo lista y mostrar la versión --option de ellos. (Este concepto con --no opciones se añadió en 7.19.0. Anteriormente la mayoría de las opciones fueron conmutadas de encendido / apagado en el uso repetido de la misma opción de línea de comandos.)


FUENTES: 

<http://curl.haxx.se/docs/manpage.html>



















