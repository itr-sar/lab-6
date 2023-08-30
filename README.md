# laboratorio No.6 - Backups/Crontab



#### Instrucciones:
Siga paso a paso los comandos en este documento y grabe un video de su servidor mientras realiza el laboratorio, suba su video a Youtube y entregue el link vía GES


### Backups
1. Cree un directorio llamado ```backup```. Aquí se guardarán los backups.
2. Crear un directorio llamado ```files```. Aquí se guardarán los archivos realizados.
3. Crear una serie de 5 archivos dentro del folder ```files``` con nombre text.# y un texto cualquiera (Ejemplo: text.1, text.2, text.3, etc.).
4. Crear el primer backup completo

   Corra el comando ```tar -czvg backup/snapshot-file -f backup/full-backup.tar.gz files/```

   Indique qué tamaño tiene el archivo tar completo (```ls -la```).

5. Crear otra serie de 5 archivos dentro del folder ```files``` con nombre text.# y con un	 texto cualquiera. (Ejemplo: text.5, text.6, text.7, etc).
6. Crear el backup incremental

   Corra el comando ```tar -czvg backup/snapshot-file -f backup/backup_inc_1.tar.gz files/```

   Indique el tamaño que tiene el nuevo archivo (ls -la)

   ¿Es menor o mayor? Justifique su respuesta al entregar el script en clase

7. Si necesita recuperar los archivos del backup sólo necesita descomprimir la información en los archivos ```*.tar.gz ``` en el directorio deseado:

   Corra el comando ```tar -xzvg backup/full-backup.tar.gz```

   Corra el comando ```tar -xzvg backup/backup_inc_1.tar.gz```

### Crontabs
1. Ingrese al crontab de su usuario con el comando: ```crontab -e```
2. Escriba la instrucción para que cada día a las 2:30 de la mañana verifique el espacio del disco usado y disponible y envíe esta información a un archivo llamado ```diskspace.output.``` (Hint: para verificar el espacio del disco puede utilizar el comando df).
3. Realice un script que, en su directorio de usuario ```/home/user/)```,  cada 5 minutos haga lo siguiente:

   Corra el comando ```ls-la``` desde el directorio anterior.
   Adjunte la fecha actual y hora cada vez que se ejecute.
   Corra el comando ```du -h``` y en su reporte final indique que realiza este comando.


### Extras
Realice la configuración necesaria para que crontab le envíe notificaciones de los comandos a su correo, esto puede hacerlo con Postfix o SMTP.

