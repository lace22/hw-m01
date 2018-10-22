1. **Quin/s paquet/s dels repositoris del sistema operatiu cal instal.lar i per a què serveixen?**
    El **Tkinter**, que fa posible obrir finestres amb Python
  

2. **Quin/s paquet/s de llibreries de python s'han d'instal.lar i per a què serveixen?**
    - **numpy** Serveix per afegir mes funcions matemàtiques
    - **matplotlib** Serveix per dibuixar gráfics


3. **Expliqueu què es fa en cada part de la transacció del nostre programa python:**

	- **Entrada:** S'agafen les dades de L'API del bicing (https://www.bicing.cat/current-bikes-in-use.json) al bucle de la linea 6
	- **Emmagatzematge:** Ho guarda a la variable ```databicing=[]```
	- **Processament:** A partir de la linea 20, obre el csv, es salta la primera columna, i fa el gráfic amb la tercera columna
	- **Sortida**: Mostra la gráfica amb   ```plt.show()```

4. **Què hauríem de canviar al codi per tal que en comptes de mostrar les bicicletes totals en ús ens mostrés només les bicicletes elèctriques en ús?**
    - Es canvia la linea 20 de
        ```python
        dades = numpy.genfromtxt('databicing.csv',delimiter=',', skip_header=1, usecols=(3))
        ```
        per
        ```python
        dades = numpy.genfromtxt('databicing.csv',delimiter=',', skip_header=1, usecols=(2))
        ```

5. **Canvieu ara els següents paràmetres del nostre programa python i copieu aquí el programa sencer una vegada modificat i comprovat que fa el que ha de fer. També copieu aquí les dades que s'han emmagatzemat al fitxer:**

   - Feu que faci 30 iteracions en comptes de 10
        - Es canvia ```while iteracio <= 10:``` per ```while iteracio <= 29:```     
   - Canvieu el títol de la gràfica de 'Bicing' pel vostre nom i cognoms
        - ES canvia ```plt.title('Bicing')``` per ```plt.title('Kyle Muñoz Andrades')```

***DADES EMMAGATZEMADES:***
```    
error,bikesInUsage,electricalBikesInUsage,mechanicalBikesInUsage,dateTime
0,450,4,446,2018-10-22 12:38:15
0,450,4,446,2018-10-22 12:38:17
0,451,4,447,2018-10-22 12:38:18
0,451,4,447,2018-10-22 12:38:20
0,451,4,447,2018-10-22 12:38:21
0,452,4,448,2018-10-22 12:38:23
0,453,4,449,2018-10-22 12:38:24
0,455,4,451,2018-10-22 12:38:26
0,453,4,449,2018-10-22 12:38:27
0,454,4,450,2018-10-22 12:38:29
0,452,4,448,2018-10-22 12:38:30
0,453,4,449,2018-10-22 12:38:32
0,453,4,449,2018-10-22 12:38:33
0,452,4,448,2018-10-22 12:38:35
0,453,4,449,2018-10-22 12:38:36
0,456,4,452,2018-10-22 12:38:38
0,456,4,452,2018-10-22 12:38:39
0,454,4,450,2018-10-22 12:38:41
0,453,4,449,2018-10-22 12:38:42
0,453,4,449,2018-10-22 12:38:44
0,454,4,450,2018-10-22 12:38:45
0,455,4,451,2018-10-22 12:38:47
0,455,4,451,2018-10-22 12:38:48
0,456,4,452,2018-10-22 12:38:50
0,456,4,452,2018-10-22 12:38:51
0,455,4,451,2018-10-22 12:38:53
0,454,4,450,2018-10-22 12:38:54
0,458,4,454,2018-10-22 12:38:56
0,459,4,455,2018-10-22 12:38:57
0,457,4,453,2018-10-22 12:38:58
```
	
***CODI FINAL:***
```python
import requests
import time
import csv
databicing=[]
iteracio=0
while iteracio <= 29:
	databicing.append(requests.get("https://www.bicing.cat/current-bikes-in-use.json").json())
	time.sleep(1)
	iteracio=iteracio+1
	print("Petició Nº:"+str(iteracio))
	print("  Dades: "+str(databicing[iteracio-1]))
titols = databicing[0].keys()
print(databicing)
with open('databicing.csv', 'w') as fitxer:
    punter = csv.DictWriter(fitxer, titols)
    punter.writeheader()
    punter.writerows(databicing)
import numpy
from matplotlib import pyplot as plt
dades = numpy.genfromtxt('databicing.csv',delimiter=',', skip_header=1, usecols=(3))
plt.plot(dades)
plt.title('Kyle Muñoz Andrades')
plt.ylabel('Bicis')
plt.xlabel('Temps')
plt.show()
```

	
