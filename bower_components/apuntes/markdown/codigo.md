
CODIGO Syntax HighLighter
-------------------------

Es conveniente enmarcar las teclas, botones, código, comandos, facilitando así su visualización y mejorando su aprendizaje. Se puede resaltar trozos de texto o bien lineas enteras y se realiza de la misma forma, envolviendo la linea con doble apertura de comillas simples.

La tecla es la siguiente: 

![](https://raw.githubusercontent.com/zapcode/apuntes/master/imgs/tecladomdresaltarkey.jpg)


CHEATSHEET:

EJEMPLO | ATRAPADO | RESALTA
--------| ------ | ------
``` `npm install bower` ```| ENTRE ```` ` ``` | EN LA LINEA
```  ``` x ``` ```| ENTRE ```  ``` y ``` ``` | BLOQUES
```  ```javascript ``` ``` | RESALTADO MÁS PRECIOSO | BLOQUES



### RESALTADO EN UNA LINEA:

Para marcar contenido a resaltar como código se usa
el símbolo: 

# ESCRIBIENDO:

```
`Enmarcar` texto es `sencillo`.
```
# SALIDA SE VE:
``` `Enmarcar` ``` ´texto´ es  `sencillo`.
-----------------------------------

# ESCRIBIENDO:
```
`Enmarcar la linea también`.
```
## SALIDA SE VE:
`Enmarcar la linea también`
==========================
```
`esto es texto enmarcardo` y esto está sin marcar

```


```
Presiona `CTRL` + `+`  PARA HACER ZOOM.
```
Salida visual:

Presiona `CTRL` + `+`  PARA HACER ZOOM.
--------------------------------------

### BLOQUE DE CODIGO:

Utilizaremos 3 comillas ``` ``` ``` para enmarcar el bloque sin especificar lenguaje

```
```
var puntos = 11;
if (esGuay){
return true
}
``````
NOS HACE LA SALIDA:

```
var puntos = 11;
 //comentario
 if (esGuay){
return true
}

```
# INDENTACIÓN ENCUADRA EL CODIGO TAMBIÉN.
## 4 ESPACIOS SEÑALA QUE ES CODIGO.

Seleccionamos el trozo de código y pulsamos `TAB` nos generara 4 espacios
exactos lo necesario para que se ponga en modo código igual que con las comillas.

```
    var nombre = "pepe";
    console.log(nombre.toString)
    if (nombre != "pepe") 
    {
    	tirarse un pedo
    }

```
Hace salida:

    var nombre = "pepe";
    console.log(nombre.toString)
    if (nombre != "pepe") 
    {
    tirarse un pedo
    }

# MARCAR ZONAS DE CODIGO COMO ELIMINADO/INSERTADO LINEAS ROJO/VERDE:

Para resaltar las lineas dentro de una zona marcada como código de las tres formas posibles:

* Entre comillas simples.
* Entre tres comillas simples.
* Indentando 4 espacios.

simplemente pondremos un + o un - junto al primer carácter.

```
    -	var edad = 23;
    -	//comentario sobre variables
    -	var nombee = "pepe";
    +	//true
    +   10 = 20;
    +	10 = 200;

```
Simula una acción.
 
    -   var edad = 23;
    -	//comentario sobre variables
    -	var nombee = "pepe";
    +	//true
    +	10 = 20;
    +	10 = 200;



### UTILIDADES

Escribiendo algo tan sencillo como esto:

Clonar un repo de Bitbucket:

	git clone https://zapcode@bitbucket.org/zapcode/curso-backbonejs.git

Clonar uno de github:





### BLOQUE DE CÓDIGO ESPECÍFICO:

```
```javascript 

var puntos = 11;
if (esGuay){
return true
}
``````

##### NOS HACE LA SALIDA:

```javascript
var puntos = 11;
if (esGuay){
return true
}
```






