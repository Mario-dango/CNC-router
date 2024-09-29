# Universal G-Code Sender

Para mandar los archivos .grbr al arduino, utilizaremos UGS(Universal G-Code Sender), es un software para g-code gratuito y completo que se utiliza para interactuar con controladores CNC avanzados como GRBL , FluidNC, TinyG, g2core y Smoothieware. 

![image](https://github.com/user-attachments/assets/b27aa510-2149-4a15-8652-141435469bc9)

## Descargar el programa

El link de descarga del programa es [este](https://winder.github.io/ugs_website/download/).

Una vez descargado el archivo, descomprimimos el .zip, ejecutamos ugsplatform64.exe y se instalará el programa.


## Como usar el programa

Lo primero es cargar  el archivo conteniendo el código, que puede ser .gcode o .txt . Si el código fué generado con FlatCAM será .gcode, y tendrá el nombre que hayamos elegido al exportarlo. Para esto se debe ingresar a File → Open. Se buscará el archivo correcto en la ventana emergente, y veremos que se abre una ventana de edición.

![image](https://github.com/user-attachments/assets/9288189a-60b5-4327-89e0-66b07eb046da)

Allí podremos ver y editar, si hiciera falta, las instrucciones.
El siguiente paso será conectarnos con la CNC.  En la parte superior izquierda de la interfaz encontraremos las opciones “Firmware”,“Port” y “Baud”. En nuestro caso, tendremos que elegir GRBL en la primera, 115200 en la última, y el puerto en el que esté nuestro Arduino en la segunda.

![image](https://github.com/user-attachments/assets/d18ec2f1-d5c9-471d-aa37-4544badc6afa)

Cuando completemos estos pasos podremos controlar manualmente nuestra máquina y ejecutar nuestro código. La interfaz nos permitirá monitorear el estado de la CNC y hacer correcciones en tiempo real.
