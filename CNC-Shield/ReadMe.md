# CNC Shield

El CNC Shield es una placa de expansión diseñada para placas Arduino (como el Arduino Uno) que permite el control de motores paso a paso y la gestión de herramientas en máquinas CNC (Control Numérico por Computadora) e impresoras 3D. Simplifica la conexión de componentes electrónicos y la construcción de proyectos de mecanizado.

![image](https://github.com/user-attachments/assets/552acaa5-08d4-438c-a52f-11e0224c7ea6)

## Funcionamiento del CNC Shield

Interfaz de Conexión: Se monta sobre un Arduino, permitiendo que este controle el shield a través de pines de expansión.

Alimentación: Conecta a una fuente de alimentación externa (12V a 36V) para alimentar los motores y el Arduino.

Control de Motores: Los drivers (como A4988 o DRV8825) se instalan en el shield y gestionan el movimiento de los motores paso a paso, donde el Arduino envía señales a los pines de los drivers para activar el movimiento.

Señales de Control: Los pines D2 a D7 controlan los motores: D2-D4: Pines de paso para los ejes X, Y y Z. D5-D7: Pines de dirección para los ejes X, Y y Z.

Gestión de Límite y Homing: Los pines D9, D10 y D12 se conectan a interruptores de límite. Cuando se activan, indican al Arduino que se ha alcanzado el final del recorrido, evitando sobreesfuerzos y permitiendo el homing.

Control del Husillo y Refrigeración: Grbl usa los pines D13 y A3 para activar el husillo y el refrigerante. El pin D11 controla la velocidad del husillo mediante PWM.

Interfaz de Usuario: Se pueden conectar botones físicos para iniciar, pausar y reiniciar operaciones, facilitando el control manual.

Ejecución de Comandos: El firmware Grbl interpreta comandos G-code desde un software de control, dirigiendo el movimiento de la máquina y la activación del husillo.

## Driver
Un driver para CNC es un componente electrónico que actúa como intermediario entre el controlador CNC y los motores (generalmente paso a paso o servomotores) que mueven las partes mecánicas de la máquina. Su función principal es recibir las señales de control (pulsos y dirección) desde el controlador y convertirlas en las corrientes y voltajes necesarios para accionar los motores. Los drivers que estamos utilizando son los A4988

![image](https://github.com/user-attachments/assets/a357146e-324d-4fac-b210-b60c5b15e47a)

### 4.2.1 Funciones principales del driver CNC:

Control de corriente: Este regula la corriente suministrada al motor para protegerlo y garantizar un movimiento suave.

Ajuste de microstepping: En motores paso a paso, el driver puede dividir cada paso en fracciones más pequeñas, proporcionando mayor precisión de posicionamiento.

Protección: Estos protegen al motor de sobrecorriente, sobrecalentamiento o cortocircuitos.

![image](https://github.com/user-attachments/assets/38773eaf-5d04-47a1-8cee-0c96fc1ad10d)

## 4.3 Configuraciones previas del software Grbl

$0=10     Step pulse, microseconds

$1=25     Step idle delay, milliseconds

$2=0     Step port invert, mask

$3=0     Direction port invert, mask

$4=0     Step enable invert, boolean

$5=0     Limit pins invert, boolean

$6=0     Probe pin invert, boolean

$10=1     Status report, mask

$11=0.010     Junction deviation, mm

$12=0.002     Arc tolerance, mm

$13=0     Report inches, boolean

$20=0     Soft limits, boolean

$21=0     Hard limits, boolean

$22=1     Homing cycle, boolean

$23=0     Homing dir invert, mask

$24=25.000     Homing feed, mm/min

$25=500.000     Homing seek, mm/min

$26=250     Homing debounce, milliseconds

$27=1.000     Homing pull-off, mm

$30=1000.     Max spindle speed, RPM

$31=0.     Min spindle speed, RPM

$32=0     Laser mode, boolean

$100=250.000     X steps/mm

$101=250.000     Y steps/mm

$102=250.000     Z steps/mm

$110=500.000     X Max rate, mm/min

$111=500.000     Y Max rate, mm/min

$112=500.000     Z Max rate, mm/min

$120=10.000     X Acceleration, mm/sec^2

$121=10.000     Y Acceleration, mm/sec^2

$122=10.000     Z Acceleration, mm/sec^2

$130=200.000     X Max travel, mm

$131=200.000     Y Max travel, mm

$132=200.000     Z Max travel, mm

