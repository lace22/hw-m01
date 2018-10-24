# Diagnostico.

Lo primero que hicimos, es quitar los tornillos del panel lateral del ordenador, a veces es necesario destornillador, otras se pueden sacar con la mano.
Para saber que tapa hay que sacar, en caso de no haber ventana, la tapa al lado contrario de los conectores es la correcta.

Después se nos enseñó el simbolo de la corriente continua y alterna de un tester
![alt text](https://github.com/lace22/hw-m01/blob/master/draw1.png?raw=true "Logo Title Text 1")
Se nos explicó como se cambia la pasta térmica de la CPU, quitando primero el disipador mirando su correspondiente manual, limpiando la pasta anterior, y con un plastico duro aplicar la nueva pasta.
Después con el tester, probamos con el modo continuidad si algunos objetos pasaban electricidad.
Todo lo que está en el panel frontal del ordenador, va enchufado a unos pines de la placa dedicado a ello, y esta es la parte mas díficil de montar ya que cada placa es diferente, los conectores son muy pequeños, y hay muchos. Como queríamos hacer la prueba de continuidad con el botón de encendido, fuimos al manual de la placa para ver que pines eran exactamente.
Ejemplo de conectores de placa.
![alt text](https://proxy.duckduckgo.com/iu/?u=https%3A%2F%2Ftse2.mm.bing.net%2Fth%3Fid%3DOIP.cPieVjHjMpsI-iARnO6Q4AHaHo%26pid%3D15.1&f=1 "Logo Title Text 1")



Desenchufamos el botón de encender y efectivamente, funcionaba con el test de continuidad.
En caso de que el botón de encendido sea el problema, simplemente enchufar el botón de reiniciar en los pines para el botón de encender.
Después enchufamos el cable ATX de 24 pines al tester especial y vimos que un pin no llegaba a dar el voltaje adecuado.
Para acabar, con un clip haciendo puente entre el pin PWR_OK y el 5VSB podemos mantener la fuente de alimentación encendida y podemos probar voltajes con un tester tradicional

![alt text](https://proxy.duckduckgo.com/iu/?u=https%3A%2F%2Fi.stack.imgur.com%2FVZS6f.jpg&f=1 "FDSFS")

