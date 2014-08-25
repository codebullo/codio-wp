
## FTP TARGET TYPE

Le permite desplegar a cualquier servidor FTP. Debe suministrar los habituales datos de acceso FTP.

![](https://codio.com/s/img/docs/deploy-ftp-6ca0b770.png)

#### RUTA BASE

Se recomienda configurar ruta de base para servidores remotos como se [describe aqui](https://codio.com/s/docs/deployment/basepath). Esto será util cuando se utiliza la [vista previa](https://codio.com/s/docs/ide/inline-preview).

#### ESPECIFICACIÓN DE PUERTO DIFERENTE A 21 POR DEFECTO

Si desea anular el puerto FTP predeterminado (21), entonces usted puede agregar el puerto después del nombre del dominio/servidor, así:

	ftp.198.93.920.3: 9002

#### MODE DE TRANSFERENCIA

    FTP can operate in 'Active' or 'Passive' mode. Codio will attempt to
    connect in passive mode by default. If it fails, then it will
    automatically try active mode. If that fails then 
    you will get an error.	


FTP puede funcionar en "modo activo" o "pasivo". Codio intentará conectar en modo pasivo de forma predeterminada. Si falla, entonces se tratará de forma automática el modo activo. Si eso no funciona por lo que recibirá un error.


    However, if you get an error then try changing the setting to Active. 
    This will ensure that Codio will only try to connect in active 
    mode without a risk of confusing the target server.

Sin embargo, si se produce un error y luego intente cambiar la configuración de Active Directory. Esto asegurará que Codio sólo intentará conectarse en modo activo sin riesgo de confusión por parte del servidor de destino.


