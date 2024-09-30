# Sensores de fin de carrera

## Propósito

Este grupo tiene como propósito la planificación y realización de: la ubicación de los sensores fin de carreras, el diseño y armado de los soportes para los sensores, y como agregar estos sensores al shield de la CNC.

## Modelo utilizado

El modelo de placa que utilizamos es el [Optical Limit Sensor Endstop Reprap 3D Ramps 1.4](https://botland.store/limit-sensors-for-3d-printers/2659-optical-limit-sensor-endstop-reprap-3d-ramps-14-5904422359195.html#). Que utiliza el sensor [**TCST2103**](https://www.alldatasheet.es/datasheet-pdf/pdf/26411/VISHAY/TCST2103.html). 

![image](https://github.com/user-attachments/assets/2927b938-49a8-494d-b053-6a92b06d66e7)


### TCST2103

Este es un sensor PullDown, normalmente abierto.

Esto significa que, cuando el banderín detecta vamos a tener 1 y cuando el banderín no detecta vamos a tener 0.  

**Características**

Tipo de sensor: Sensor óptico transmisivo.

Dimensiones: 24.5 mm (largo) x 6.3 mm (ancho) x 10.8 mm (alto).

Distancia del espacio entre emisor y receptor: 3.1 mm.

Corriente de salida típica: 4 mA.

Filtro de bloqueo de luz diurna: Integrado.

Longitud de onda del emisor: 950 nm (infrarrojo).

Tensión de colector-emisor (máxima): 70 V.

Tensión de emisor-colector: 7 V.

Corriente de colector pico: 200 mA.

Temperatura de operación: -55°C a +85°C.

Capacidad de disipación de potencia: 250 mW.

Tiempo de encendido/apagado: 10 µs encendido / 8 µs apagado.

## Pines de alimentación.

Debido a un problema con la cantidad de pines de alimentación que el shield que la CNC poseia, se tuvo que armar una placa aparte para poder conectar todos los cables de los sensores a el Shield.

![IMG-20240923-WA0002](https://github.com/user-attachments/assets/2bf7665b-61c3-4233-892c-3ec93471a5d7)
![IMG-20240923-WA0001](https://github.com/user-attachments/assets/9aa0ff8a-7539-438b-9a1f-01d96179be53)

## Soportes.

Los soportes para los sensores fin de carrera son elementos cruciales en la instalación de sistemas automatizados. Estos garantizan que los sensores estén correctamente posicionados y alineados, lo que es fundamental para el funcionamiento preciso de la máquina.

Para crear estos soportes, se midieron las ubicaciones y tamaños correspondientes en cada uno de los ejes de coordenadas, luego se realizaron los soportes a partir del programa de modelado 3D [Tinkercad](https://www.tinkercad.com/)
, y se imprimieron con PLA y ABS. Para el laminado de la impresion se utilizo el programa [Bambu Lab](https://bambulab.com/en-us/download/studio).

![image](https://github.com/user-attachments/assets/3149863d-df30-4ada-83e2-d8cb9f027ef5) ![image](https://github.com/user-attachments/assets/2b5ba92f-57b1-4365-89ce-cb53e3129a67)



