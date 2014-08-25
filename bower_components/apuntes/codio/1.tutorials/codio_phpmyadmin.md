## Instalación de `PHPmyAdmin`

* Requisitos: PHP, Apache y MySQL y arrancados.
	* Comprueba si lo tienes instalado con comando `parts list`
    * Si no lo tienes, Instalalos con:
    		parts install php5 php5-apache2 php5-pdo-mysql php5-zlib mysql

* Instalamos con parts:
```
	parts install phpmyadmin
```
* Accedemos en la URL que nos devuelve la terminal:

```
// Reinicia apache para poder acceder a phpmyadmin.
// Admin config archivo esta en
/home/codio/.parts/packages/phpmyadmin/4.1.7/phpmyadmin/{phpmyadmin_config} 
PhpMyAdmin URL is http://your-domain-name:3000/phpmyadmin 
```
Descubre tu dominio de codio.com en preview `proyect index` o `BOX URL`, 
En mi caso entro en: 
```
http://mailbox-spoon.codio.io:3000/phpmyadmin/
```
Ya nos aparece para entrar, escribimos usuario: wordpress y password
