# Sensores de fin de carrera

## Propósito

Este grupo tiene como propósito la planificación y realización de: la ubicación de los sensores de carreras, el diseño y armado de los soportes para los sensores, y como agregar estos sensores al shield de la CNC.

## Modelo utilizado

El modelo de placa que utilizamos es el [Optical Limit Sensor Endstop Reprap 3D Ramps 1.4](https://botland.store/limit-sensors-for-3d-printers/2659-optical-limit-sensor-endstop-reprap-3d-ramps-14-5904422359195.html#). Que utiliza el sensor [**TCST2103**](https://www.alldatasheet.es/datasheet-pdf/pdf/26411/VISHAY/TCST2103.html). 

![image](https://github.com/user-attachments/assets/2927b938-49a8-494d-b053-6a92b06d66e7)


### TCST2103

Este es un sensor PullDown normalmente abierto

Esto significa que cuando detecta el banderín vamos a tener 0 y cuando no detecta el banderín vamos a tener 1.  

## Pines de alimentación

Debido a un problema con la cantidad de pines de alimentación que el shield que la CNC poseia, se tuvo que armar una placa aparte para poder conectar todos los VCC y GND.

![IMG-20240923-WA0002](https://github.com/user-attachments/assets/2bf7665b-61c3-4233-892c-3ec93471a5d7)
![IMG-20240923-WA0001](https://github.com/user-attachments/assets/9aa0ff8a-7539-438b-9a1f-01d96179be53)
