# iotGrupo15

Esta aplicación será una demo del sistema de almacenamiento y descontaminación de comida para personas vulnerables que describimos en clase.

## Procedimiento

La raspberry con función de sensor, detectará una tarjeta NFC para simular que se abren las puertas del frigorífico o armario (se simulará con un objeto metálico y el imán junto a los dos magnetic switches). En cuanto se cierren las puertas comenzará un contador de 48 segundos (epara el correcto uso en la vida real habría que cambiar este parámetro a 48 horas).
Cuando se complete este se enviará una señal a la raspberry avisadora, que irá mostrando el paso del tiempo en la ledbar y cuando se complete, sonará un pitido. A partir de este momento, se podrá abrir con la segunda tarjeta NFC.
La raspberry sensor recoje datos y los manda a una BD en Grafana.

## Comenzando 🚀

_A continuación, se explican los pasos a seguir para la correcta utilización de la aplicación._


### Pre-requisitos 📋

Para el funcionamiento correcto de la aplicación, es necesario disponer de:
  - Dos Raspberry Pi (https://www.raspberrypi.org/)
  - Dos Grove hat (https://wiki.seeedstudio.com/Grove_Base_Kit_for_Raspberry_Pi/)
  - Dos Botones (https://wiki.seeedstudio.com/Grove-Button/)
  - Una Led Bar (https://wiki.seeedstudio.com/Grove-LED_Bar/)
  - Un magnetic switch (https://wiki.seeedstudio.com/Grove-Magnetic_Switch/)
  - Un buzzer (https://wiki.seeedstudio.com/Grove-Buzzer/)
  - Imán electrónico (https://wiki.seeedstudio.com/Grove-Electromagnet/
  - Cables PWM

### Instalación 🔧

_Clonar repositorio_
  Primero habrá que clonar el repositorio de github desde este link:
```
    https://github.com/Sanrro10/iotGrupo15/
```
  En caso de querer clonar desde la consola, utilizaremos estos comandos:
```
  git remote add origin https://github.com/Sanrro10/iotGrupo15.git
  git push -u origin master
  ```
  
En una Raspberry, que hará de sensor, tendremos conectados un botón, el imán electrónico y un magnetic switch e instalaremos el código correspondiente al sensor. 
En la otra, el avisador, conectaremos el resto de componentes e instalaremos el código de la carpeta avisador.
Ejecutamos el código de ambas y las conectamos por bluetooth.
En una simulación más cercana a una aplicación real de este proyecto, ambos programas estarán en crontab puesto que pertenecerian a dispositivos sin interfaces dedicados exclusivamente a este programa. 
## Construido con 🛠️

_Menciona las herramientas que utilizaste para crear tu proyecto_

* [Python](https://es.python.org) - Lenguaje de programación.
* [JupyterLab](https://jupyter.org) - Framework
* [Log4j](https://logging.apache.org/log4j/2.x/) - Logger
* [Travis](https://travis-ci.org/) - Tester e implementador


## Autores ✒️

* **Marcos Barcina**  [marcosbarcina@opendeusto.es]
* **Danel Rey**  [danel.rey@opendeusto.es]
* **Iñigo Gonzalez de San Román** [i.glzsr@opendeusto.es]
