# Cambiar la contrasena de Root cuando no la tienes

Hay dos maneras sencillas de hacer esto, con Live Image o sin ella.

## Con Live Image

- Arrancamos una Live Image del sistema operativo
- Cuando haya arrancado, abrimos una terminal, y usamos su para entrar como root (No pedira contrasena)
- Creamos un directorio para montar el sistema de archivos de tu instalacion, por ejemplo
mkdir /mnt/sysimage
- Montamos el sistema de archivos en la carpeta con
mount /dev/sda1 /mnt/sysimage
hacemos chroot a la instalacion
chroot /mnt/sysimage
Usamos el comando passwd, y ya podemos reiniciar y arrancar nuestro sistema operativo

## Sin Live Image
- Cuando estemos en el GRUB, pulsaremos e, y buscaremos la linea que empieza con "linux" "linux16" o "linuxefi"
- Al final de la linia anadiremos un rw init=/bin/bash
- Usaremos F10 O Control+X para arrancar.
- Cuando arranque usaremos el comando passwd para cambiar la contrasena de root