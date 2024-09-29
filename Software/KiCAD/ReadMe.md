# AREAS

## Archivos Necesarios de KiCAD

Luego de diseñar nuestra PCB, necesitaremos exportar ciertos archivos necesarios para importarlos a FlatCAM. Necesitamos archivos Gerber individuales, uno para cada capa, archivos Excellon para perforaciones, y un archivo Gerber para el borde de la placa.

### Generar archivos Gerber

Una vez tenemos nuestra PCB, entraremos a "File", dentro de este, en "Fabrication Outputs" seleccionaremos "Gerber(.gbr)".

![GRB1](https://github.com/user-attachments/assets/3459444c-70cc-4b97-8a11-9c8aae53d16f)

#### Configuración

![image](https://github.com/user-attachments/assets/764f7d1c-f3f4-4b46-84d7-7ec784fed6d9)

**Plot format:** Tipo de archivo a generar. Nosotros usamos Gerber.

**Output directory:** Carpeta en la que se generan los archivos. Si empieza con “.” es una dirección relativa, y la carpeta estará dentro de la carpeta del proyecto.

**Include Layers:** Capas a exportar. Solo marcaremos F. Cu , y B.Cu si queremos trabajar ambos lados de la placa. 

#### Configuración General
***ACTIVADAS***

**Check zone fills before plotting:** Antes de generar los archivos, se revisarán las zonas de cobre. Dejar activado para prevenir errores. 

**Use drill/place file origin:** Permite elegir si usar el origen (de coordenadas) predeterminado o uno elegido por nosotros.  Dejar activado y correr el diseño a la esquina superior izq.

***DESACTIVADAS***
**Plot on All Layers:** Capas que se incluirán en todos los archivos de las capas seleccionadas en la lista anterior. No seleccionar ninguna. 

**Plot Drawing Sheet:** Imprime el marco y título. Dejar desactivado.

**Plot Footprint Values:** Imprime el valor de cada huella, en la capa correspondiente. Dejar desactivado.

**Plot Reference Designators:** El nombre de cada huella se imprimirá, en la capa correspondiente. Dejar desactivado.

**Plot footprint text:** Imprime el texto asociado a cada huella, en la capa correspondiente. Desactivar esta opción anula las dos anteriores. Dejar desactivado.

**Force plotting of invisible values / refs:** Las opciones anteriores no imprimían el texto que estaba oculto. Si se activa esto, también se imprimirá. 

**Plot Edge.Cuts on all layers:** Añade los bordes de la placa a todos los archivos. Dejar desactivado.

**Sketch pads on fabrication layers:** Cambia el dibujo de pads en las capas de fabricación, las que contienen los componentes. Nosotros no las usaremos.

**Drill marks:** Configuración necesaria para otros formatos. No es necesaria para Gerber.

**Scaling:** No compatible con Gerber. 

**Plot mode:** No compatible con Gerber.

**Mirrored plot:** Permite espejar el dibujo. No compatible con Gerber.

**Negative plot:** Invierte el dibujo, es decir, deja vacío el espacio a trabajar, y marca el espacio vacío. No compatible con Gerber.

**Tent vías:** No es importante para nuestro CNC. Sirve para capas de protección.

#### Gerber Options

**Use Protel filename extensions:** Permite elegir la terminación de los archivos Gerber: .gbr o .GBL y otros. Diferencia entre cada archivo:
*Archivo .gbr (Gerber):*
Propósito: El archivo ".gbr" es una representación de los datos de las capas de un PCB en formato Gerber. Los archivos Gerber son utilizados para describir las diferentes capas del diseño de un circuito impreso, como las capas de trazado, soldadura, y máscara de soldadura.
*Archivo .gbl (Gerber Bottom Layer):*
Propósito: El archivo ".gbl" específicamente representa la capa inferior (bottom layer) de un PCB. Es uno de los archivos generados cuando se exporta el diseño en formato Gerber.

**Generate Gerber job file:** Genera un .grbjob junto con los demás .grb 
**Subtract soldermask from silkscreen:** No es necesario. 
**Coordinate format:** *Formato de coordenadas:* 4,5 unid. por mm. o 4,6 unid. por mm. 
**Use extended X2 format:** Usar Gerber X1 o X2. 
**Include netlist attributes:** Añade información útil, principalmente de conexiones, al archivo Gerber. Si es X1 la pone como comentarios.
**Disable aperture macros:** Para algunos visores de Gerber o programas de diseño que presenten errores. Dejar desactivado.

### Generar archivos Excellon

Dentro de la PCB, en "Files", seleccionaremos "Fabrication Outputs" y ahí crearemos un archivo Drill(.drl).

#### Configuración

**Output folder:** Elegir carpeta de destino. Si empieza con “.” es una dirección relativa, y la carpeta estará dentro de la carpeta del proyecto.

**rill file format:** Elegir entre Excellon y Gerber X2. Nosotros usamos Excellon.

**Mirror Y axis:** Espeja el eje y. Puede ser útil si vamos a hacer una pcb de ambos lados. 

**Minimal header:** Reduce el header, datos al inicio del archivo. Dejar desactivado.

**PTH and NPTH in single file:** Junta los pads no revestidos con los revestidos, cuando normalmente los exporta en archivos separados. Nosotros al momento de fabricar no haremos ninguna diferencia, por lo que esta configuración no es importante. 

**Oval holes drill mode:** Cambia la forma en la que se escriben los agujeros ovalados en el archivo excellon.

**Map file format:** Elige el formato en el que se creará un mapa de taladrado. 

**Drill origin:** Permite elegir si usar el origen (de coordenadas) predeterminado o uno elegido por nosotros. Dejar activado y correr el diseño a la esquina superior izq.

**Drill units:** Elige entre mm y pulgadas. Usar mm.

**Zeros format:** Elige cómo se escriben los ceros en el programa de salida. 

*Los tipos de formato son:*

Decimal format: Esta opción se refiere al uso del formato decimal para representar los números en el archivo Excellon. Es un formato estándar que usa números decimales y puede o no incluir ceros a la izquierda o a la derecha según otros ajustes.

Supress leading zeros: Esta opción suprime los ceros a la izquierda de los números. Por ejemplo, el número 005 se representaría simplemente como 5.

Supress trailing zeros: Esta opción suprime los ceros a la derecha de los números después del punto decimal. Por ejemplo, el número 1,500 se representaría como 1,5.

Keep zeros: Esta opción mantiene todos los ceros a la izquierda y a la derecha en los números. Por ejemplo, 005 se mantendría como 005, y 1,500 se mantendría como 1,500.

## Visualizar archivos gerber dentro de KiCAD

![image](https://github.com/user-attachments/assets/15c6982c-09f5-4e3c-ab84-0874b40eb4fa)
