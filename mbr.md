# Master Boot Record

El Master Boot Record es una partición de 512 bytes ubicada en el primer sector de un dispositivo particionado en MBR.

## Contenido
### Gestor de arranque
Los primeros 446 bytes de la partición están dedicados al arranque del disco duro. 
Cuando se enciende el ordenador, la bios hace muchos tests de que todo funcione correctamente, al terminar todo esto, la BIOS busca en los dispositivos de almacenamiento el gestor de arranque, cuando lo encuentra, la bios empieza el proceso de arrancar el sistema operativo usando la información del gestor de arranque.
### Tabla de Particiones
La tabla de particiones empieza en el byte 446 y ocupa 64 bytes, contiene cuatro registros de 16 bytesm que definen las 4 particiones primarias que puede tener un disco duro en MBR.
### Firma
La partición MBR contiene un identificador del disco duro, para que el sistema operativo pueda identificar los diferentes dispositivos.