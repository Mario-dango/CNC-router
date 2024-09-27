# AVANCES SEMANA POR SEMANA EN LOS SENSORES DE FIN DE CARRERA

**SEMANA 1**

La primera semana fue de pura investigación. Sabíamos que íbamos a usar sensores ópticos infrarrojos como sensores de fin de carrera (todavía no los teníamos), así que nos pusimos a entender cómo funcionan. Leímos sobre cómo estos sensores detectan la posición al interrumpir un haz de luz infrarroja y cómo integrarlos con nuestra CNC. También revisamos varias opciones para ver cuál sería la mejor forma de conectarlos al sistema de control y asegurarnos de que funcionaran bien.

**SEMANA 2**

Esta semana fue más práctica. Analizamos dónde colocar los sensores en la CNC y tomamos medidas detalladas para asegurarnos de que los sensores ópticos infrarrojos tuvieran suficiente espacio y que el haz de luz no tuviera interferencias. La meta era colocarlos en puntos estratégicos para que funcionaran correctamente cuando la CNC alcanzará sus límites.

![SFC](https://github.com/user-attachments/assets/9c5b4845-2083-458d-aa81-ee25fbbf5885) ![SFC2](https://github.com/user-attachments/assets/b0f55e8f-6b61-43e0-8fef-c68a17bdb10b)

**SEMANA 3:**

Con las medidas en mano, imprimimos en 3D los soportes para los sensores. Pero cuando fuimos a montarlos, nos dimos cuenta de que algunos soportes no se ajustaban bien o interfieren con el movimiento. Esto nos llevó a revisar y modificar los diseños, ajustando las dimensiones para que todo encaja de forma correcta.

**SEMANA 4:**

Esta semana logramos diseñar correctamente los soportes y banderines con las medidas precisas. Además, nos encontramos con un problema: había poca disponibilidad de puertos para conectar el GND, VCC y la señal de los seis sensores. Para solucionarlo, diseñamos una placa que nos permitió conectar todos estos elementos, unificando las conexiones y sacando un solo cable para cada sensor. Esto facilitó mucho la instalación y nos permitió organizar mejor el cableado.

![foto](https://github.com/user-attachments/assets/f214b320-dfd3-4eec-9c92-f9c577358a0f)  ![2024-09-27_104158](https://github.com/user-attachments/assets/bccbf383-404e-4d1e-9cdc-6316fc5d7e9d)

**Color verde: parte de información de los sensores fin de carrera.**
**Color rojo: parte del vcc.**
**Color azul: parte del gnd.**

**Semana 5**

En la última semana, instalamos definitivamente los soportes y sensores en sus posiciones finales. Nos aseguramos de que los banderines interrumpieron correctamente el haz de luz infrarroja para activar los sensores al llegar a los límites de la CNC. Con esto, terminamos nuestra parte del proyecto, y la máquina ahora puede detectar los límites de sus ejes de manera precisa.







