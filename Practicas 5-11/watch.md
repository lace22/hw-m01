# Comando Watch
El comando watch se usa para ejecutar un determinado comando a intervalos regulares. Muestra el resultado del comando en una consola completamente limpia de otros contenidos para hacer mas facil observar los cambios del output.
## Cambiar el intervalo del comando
Para cambiar el intervalo se usa el parametro `-n` acompañado de el intervalo en segundos.
Por defecto los intervalos son de dos segundos, pero usando `-n 1` el intervalo entre ejecución será de un segundo
## Ejemplo
`watch -n 1 vmstat -s`
Nos muestra información de la RAM que se actualiza cada segundo