


### COMO CREAR ENLACES:

LINK BASICO | EJEMPLO Y RESULTADO:
------------- | 
`<ENLACE>` | Esta es mi web `<http://www.soloaplicaciones.com>` 
  SALIDA:  | Esta es mi web <http://www.soloaplicaciones.com>  



LINK TÍPICO | EJEMPLO
------ | -------
`[]()` | `[Leer más](http://adam/cheat.com)`
 SALIDA: | [Leer más](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
 
 LINK TÍPICO | EJEMPLO
------ | -------

## Enlaces estilo variables:

En algunos casos puede interesarnos referirnos al mismo enlace en varias partes del documento por lo que interesa poder utilizarlo en lugar de hacer esto:

```
Recomendamos utilizar [bitbucket](https://bitbucket.org/)
para proyectos privadosy utilizar [github](https://github.com/) 
para proyectos publicos, la comunidad es mayor,
existen también editores en la nube como [Codio](https://codio.com)
y herramientas como <http://jsfiddle.net> , <https://www.digitalocean.com/pricing/> .
Recomendamos seguir a los usuarios: [Addyosmani](http://addyosmani.com/blog/) 

```
#### SALIDA: 

Recomendamos utilizar
[bitbucket](https://bitbucket.org/)
para proyectos privadosy 
utilizar [github](https://github.com/) 
para proyectos publicos, la 
comunidad es mayor, existen 
también editores en la nube 
como [Codio](https://codio.com)
y herramientas como <http://jsfiddle.net>,
<https://www.digitalocean.com/pricing/> .
Recomendamos seguir a los usuarios:
[Addyosmani](http://addyosmani.com/blog/) 



[Google]

Si escribimos esto:<br>

    `[Google]: http://google.com <br>' 
    `[Udemy]: https://www.udemy.com'

[Google]: http://google.com

[Udemy]: http://udemy.com

Luego podemos llamar a esos links así:<br>
`[Google]` <br>
[Google]

O así si queremos cambiar como se visualiza:<br>
`[Udemy][Estudia en Udemy]`<br>

[Udemy][Estudia en Udemy]

Útil en algunos casos para tener todos los enlaces
y no repetirse cuando se quiere mencionar un mismo link
además de que resulta muy compacto 
escribir `[Mi Web]` en la doc.
***