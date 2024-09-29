# AREAS

## Qué es FLATCAM

FlatCAM es una aplicación para preparar diseños de circuitos impresos para ser fabricados en una enrutadora CNC. Entre otros, puede generar G-Code para enrutamiento de aislamiento a partir de archivos Gerber generados en aplicaciones de CAD(KiCAD en nuestro caso) para circuitos impresos favoritos.

## Cómo importar archivos GERBER

Dentro de files, en Open Gerber se seleccionan los archivos ya exportados de KiCad, específicamente sus layers F_Cu.gbr o B_Cu.gbr.
Luego se deberá seleccionar el apartado de Open Excellon y de allí el archivo terminado en PTH.drl.

![image](https://github.com/user-attachments/assets/956119cf-d720-4c9e-aca8-501d38e2e0e9)

## Generación de G-CODE

### Selección del Archivo
1. **Archivo de Pistas**: Ve a *Project* y selecciona el archivo con terminación `B_Cu.grb` o `F_Cu.grb`. Configura el proceso en *Selected*.

2. **Imagen en Coordenadas**: Si la imagen no está en el origen, ajusta el *Offset*. Anota el desplazamiento para mover el archivo de perforado igual. Recuerda que cada ajuste en *Offset* se aplica inmediatamente.

### Generar Geometrías
1. **Configurar Barrido**: En *Selected*, elige *Isolation Routing*. Define el diámetro de la herramienta, número de pasadas y superposición. Activa *Combine Passes* para un único archivo.

2. **Generar Archivo**: Presiona *Generate Geometry* para crear un archivo `.grb_iso`.

### Generar Trabajo CNC
1. **Parámetros CNC**:
   - **Profundidad de Corte (Cut Z)**
   - **Altura de Desplazamiento (Travel Z)**
   - **Velocidad de Desplazamiento (Feed Rate)**
   - **Diámetro de la Herramienta (Tool Dia)** (No relevante para este paso)
   - **Velocidad de Giro (Spindle Speed)**
   - Desactiva *Corte en Múltiples Capas*.

2. **Generar Archivo CNC**: Presiona *Generate* para crear un archivo `.grb_iso_cnc`.

### Generar G-Code
1. **Exportar G-Code**: Selecciona el archivo `.grb_iso_cnc` y ajusta el *dwell* a 2-3 segundos. Puedes añadir instrucciones si es necesario. Presiona *Export G-Code*.

### Perforaciones
1. **Generar Trabajo CNC**:
   - Selecciona el archivo Excellon (.drl) en *Project* y ajusta el *Offset* si es necesario.
   - Marca las herramientas en *Tools*.
   - Configura parámetros y presiona *Generate*.

2. **Generar G-Code**: Selecciona el archivo `.drl_cnc`, ajusta el *dwell* y presiona *Export G-Code*.

### Previsualizar G-Code
Para ver cómo actuará la CNC, copia el G-Code en [NCViewer](https://ncviewer.com/).

### Generar G-Code para el Contorno
1. **Archivo de Bordes**: Selecciona el archivo `Edge.Cuts`.
2. **Configurar Herramienta y Geometría**: Genera la geometría y crea el trabajo CNC.
3. **Exportar Código**: Exporta el G-Code.

### Parámetros Adicionales
- **Cut Bit Diameter**: Diámetro de la herramienta.
- **Cutting Depth**: Profundidad de corte (considera el ancho de la placa).
- **Horizontal Cut Speed**: Comienza en 100 mm/min y ajusta según sea necesario.
- **Maximum Single-Pass Depth**: Máxima profundidad por pasada (ajustar si es necesario).
- **Number of Bridges**: Número de puentes para sujetar la placa.
- **Bridges Depth**: Aproximadamente la mitad del grosor de la placa.

### Recursos Útiles
- [FlatCAM Manual](http://flatcam.org/manual/procedures.html)
- [GRBL GitHub](https://github.com/gnea/grbl)
- [Configuración de GRBL](https://github.com/grbl/grbl/wiki/Configuring-Grbl-v0.9)
- [G-CODE](https://machmotion.com/downloads/GCode/Mach4-G-and-M-Code-Reference-Manual.pdf)
- [GERBER](https://www.ucamco.com/files/downloads/file_en/81/the-gerber-file-format-specification_en.pdf?834337316a7d266ef3ab3d03cff55fc0)
