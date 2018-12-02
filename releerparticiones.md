# Partprobe
El comando `partprobe` sirve para que el kernel re leea la tabla de particiones del disco duro
# Kpartx
Alternativamente si el partprobe no hace que sean visibles los cambios, podemos usar  
`kpartx -l archivo` para mappearlo en `/dev/mapper/loop0pX`
