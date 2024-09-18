# SSR
Este repositorio contiene el diseño y componentes para la construcción del relé de estado sólido (SSR)

![SSR-40-_clipped_rev_1](https://github.com/user-attachments/assets/ae221fad-aad4-40ed-a34b-b46e9aa6d09e)

## Esquemático

![image](https://github.com/user-attachments/assets/02d59e1e-d9cc-4307-90b1-58eacc3f9cfa)

## Componentes

### 1.**BTA08 Triac**

El triac de la serie BTA08 se utiliza para controlar la alimentación en el lado de la corriente alterna (AC). Puede manejar grandes cargas de voltaje y corriente.

- **Voltaje máximo**: 800V
- **Corriente máxima**: 8A
- .
  [BTA08.PDF](https://github.com/user-attachments/files/17043512/BTA08.PDF)

### Specs necesarias para cambiarlo:
- **Voltaje de bloqueo inverso/repetitivo**: ≥ 800V
- **Corriente máxima**: ≥ 8A
- **Sensibilidad de compuerta**: similar a la del BTA08 para garantizar una activación adecuada.

### 2. **Optoacoplador MOC3020**
El MOC3020 proporciona aislamiento entre el circuito de control de bajo voltaje y el circuito de AC de alto voltaje. Está diseñado para disparar el triac de manera segura.

- **Voltaje máximo**: 400V
- **Corriente directa máxima**: 60mA
- .
[MOC3020.PDF](https://github.com/user-attachments/files/17043585/MOC3020.PDF)

### Specs necesarias para cambiarlo:

- **Voltaje de salida**: ≥ 400V
- **Corriente de entrada directa**: ≤ 60mA
- **Tipo de acople**: compatible con triac, como los modelos MOC3021, MOC3022 o MOC3023.
  
## PCB
![image](https://github.com/user-attachments/assets/6b0cd7a1-25a2-4873-a320-1d5beb2c02fa)
Esta pcb es la segunda versión, dado que la anterior era más grande de lo que quería.


Adjunto ahora el trazado de la pcb para su realización:
![image](https://github.com/user-attachments/assets/9bc09f13-14ab-4d34-bded-ecd043558294)

[IntentoFinalSSR.pdf](https://github.com/user-attachments/files/17043709/IntentoFinalSSR.pdf)






