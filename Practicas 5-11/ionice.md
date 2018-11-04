# Comando ionice

El comando ionice nos permie asignar la prioridad de un proceso o de un comando en linux.
## Parametros del comando

| Parametros       |   Niveles         | 
| ------------- |:-------------:| 
| -c      | prioridad del 0 al 3, el 1 para tiempo real y el 3 para inactivo | 
| -n      |    Prioridad del 0 al 7, la mínima el 7 la maxima el 0   |  
| -p      |    PID del proceso al que se le quiere asignar la prioridad   | 
 
### Ejemplo

`ionice -n7 dd`
Asigna la mínima prioridad al comando `dd`