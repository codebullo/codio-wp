- ### SSH 
	- #### OpenSSH 5.9p1 Debian-5ubuntu1.4, OpenSSL 1.0.1
    - `ssh ip_host_remoto`
    	- Conexión ssh básica.
    - `ssh usuario@ip_del_ordenador_remoto`
    	- Conexión ssh básica dando usuario.
    - `/etc/ssh/sshd_config`
    	- Localización del archivo de configuración.
    - `ssh -p 4884 pepino@192.168.1.4`
    	- Conexión incluyendo `-p` número de puerto.
    -  `scp -P 8448 pepino.jpg tux@192.168.1.6:/home/tux/pepinaceo.jpg`
    	- Transmisión de una imagen local a remoto vía SSH.
    - `scp -P 8448 /home/pepino/Desktop/pepino.jpg tux@192.168.1.6:/home/tux/pepinaceo.jpg`
    	- Transmisión de una imagen local a remoto vía SSH.
    - `ssh-keygen -t rsa`
    	-  Generar las dos claves DSA
        
La sintaxis básica del comando ssh es:

`ssh user@hostname [command]`

El comando es opcional. Si se especifica en lugar de obtener un shell se ejecuta el comando en la máquina remota.

Por ejemplo podríamos hacer un ls en la máquina remota y observar su salida:

`ssh usuario1@servidor.dominio.es ls`

O realizar alguna operación mas elaborada como realizar una copia en local de un directorio remoto, como en el ejemplo:


	ssh usuario1@servidor.dominio.es "tar cf - /home/usuario1"
                                      tar xvf -


Una de las funcionalidades que le da mayor potencia al ssh es la redirección de las X. Si observas la variable de entorno DISPLAY observarás que tiene la forma localhost:n.n, esta permite que al abrir cualquier aplicación gráfica su salida se redirija al display del cliente.

    [usuario1@localhost usuario1]$ ssh usuario1@servidor.dominio.es
    [usuario1@servidor usuario1]$ echo $DISPLAY
    localhost:11.0
    [usuario1@servidor usuario1]$ xeyes&
    [usuario1@servidor usuario1]$

El comando para listar archivos de una carpeta es:

	ls 
Listamos archivos



FUENTES: 

<https://support.cdmon.com/entries/24120003-Manual-b%C3%A1sico-de-SSH>