

# WGET

GNU Wget (o simplemente Wget , anteriormente getURL ) es un programa informático que recupera el contenido de los servidores web , y es parte del proyecto GNU . Su nombre se deriva de la World Wide Web y obtener . Soporta la descarga a través de HTTP , HTTPS y FTP protocolos.

Sus características incluyen descarga recursiva, conversión de enlaces para verlas sin conexión de HTML locales, y el apoyo a los proxies. Apareció en 1996, coincidiendo con el auge de la popularidad de la Web, haciendo que su amplio uso entre Unix usuarios y de distribución con las principales distribuciones de Linux . Escrito en portátil C , Wget puede ser instalado fácilmente en cualquier sistema Unix y ha sido portado a muchos entornos, incluyendo Microsoft Windows , Mac OS X , OpenVMS , MorphOS y AmigaOS .

Se ha utilizado como base para programas gráficos como gwget para el GNOME escritorio.


## Descarga recursiva

Wget opcionalmente puede trabajar como un rastreador web mediante la extracción de los recursos vinculados de HTML páginas y descargarlos de forma secuencial, repitiendo el proceso de forma recursiva hasta que todas las páginas se han descargado o se ha alcanzado un nivel de recursividad especificado por el usuario. Las páginas descargados se guardan en una estructura de directorios que se asemeja en el servidor remoto. Esta "descarga recursiva" permite la duplicación parcial o total de los sitios web a través de HTTP. Enlaces en páginas HTML descargados pueden ser ajustados para que apunte a material descargado localmente para offline visualización. Al realizar este tipo de automático reflejo de sitios web, Wget soporta el estándar de exclusión de robots (a menos que la opción -e robots = off se utiliza).

Descarga recursiva funciona con FTP también, donde Wget emite la LISTA comando para encontrar archivos adicionales para descargar, repitiendo este proceso para los directorios y ficheros bajo el especificado en la parte superior URL . Shell-como comodines son compatibles cuando se solicita la descarga de FTP URLs.

Al descargar de forma recursiva sobre cualquiera de HTTP o FTP , Wget puede ser instruido para inspeccionar las marcas de tiempo de archivos locales y remotos, y descargar sólo los archivos remotos más recientes que los correspondientes locales. Esto permite una fácil creación de reflejo de HTTP y FTP sitios, pero se considera ineficiente y propenso a errores cuando se comparan con los programas diseñados para la creación de reflejo de la base, tal como rsync . Por otro lado, Wget no requiere software del lado del servidor especial para esta tarea.

## No interactividad

Wget es no interactivo en el sentido de que, una vez iniciado, no requiere la interacción del usuario y no necesita para controlar un TTY , pudiendo registrar su progreso en un archivo separado para una inspección posterior. De esta manera el usuario puede comenzar a Wget y cerrar la sesión , dejando el programa sin supervisión. Por el contrario, la mayoría de los gráficos o de la interfaz de usuario de texto navegadores web requieren que el usuario permanecer conectado y reiniciar manualmente descargas fallidas, que puede ser un gran obstáculo al transferir una gran cantidad de datos.

## Otras características

* Wget soporta descargas mediante proxies , que son ampliamente utilizados para proporcionar acceso web dentro de la empresa firewalls y almacenar en caché y rápidamente entregar el contenido de acceso frecuente.
* Se hace uso de conexiones HTTP persistentes cuando estén disponibles.
* IPv6 es compatible con sistemas que incluyen las interfaces adecuadas.
* SSL / TLS se admite para las descargas cifrados utilizando el OpenSSL biblioteca.
* Archivos de más de 2 GiB están soportados en sistemas de 32 bits que incluyen las interfaces adecuadas.
* La velocidad de descarga puede ser estrangulado a evitar el uso de toda la disposición de ancho de banda

