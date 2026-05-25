# Invernadero Inteligente V1


## Autor
Santiago Perdomo Moyano


## Objetivo

Diseñar una maqueta de invernadero inteligente capaz de monitorear temperatura y luminosidad, activando actuadores de forma automática según las condiciones del entorno.


## Componentes utilizados

### Sensores

- LM35 (temperatura)
- LDR (luminosidad)
- LM393 (comparador)


### Actuadores

- Ventilador de 5V
- Sistema de iluminación mediante LEDs de 12V


## Funcionamiento

El sensor LM35 monitorea continuamente la temperatura.

El sistema fue calibrado para activar el ventilador cuando la temperatura alcanza aproximadamente 35°C.

El comparador LM393 compara la señal proveniente del LM35 con una referencia previamente ajustada.

Cuando la temperatura supera el umbral configurado, el LM393 cambia de estado y activa el ventilador de 5V.

La iluminación se controla mediante una LDR.

Cuando la intensidad lumínica disminuye por debajo del nivel establecido, se activan los LEDs de 12V para complementar la iluminación del invernadero.

## Calibración del sistema

Antes de construir el circuito físico, se realizó una simulación en Proteus para validar el comportamiento del sistema.

En la simulación se ajustó el potenciómetro hasta encontrar el punto en el que el ventilador se activaba cuando la temperatura alcanzaba aproximadamente 35°C.

El punto de activación encontrado fue cercano al 7% del recorrido del potenciómetro, equivalente aproximadamente a 700 ohmios.

Después de validar este valor en Proteus, se calibró el circuito físico utilizando un multímetro para ajustar el potenciómetro al valor requerido.


## Aprendizajes obtenidos

- Funcionamiento de sensores analógicos.
- Uso del LM393 como comparador.
- Integración entre sensores y actuadores.
- Diseño básico de sistemas automáticos.
- Comprensión de la lógica de control sin microcontroladores.

## Problemas encontrados

- La calibración del umbral de temperatura requirió pruebas en simulación y ajuste físico con multímetro.
- El valor de activación dependía del ajuste preciso del potenciómetro.
- El sistema no registraba datos históricos, solo activaba actuadores en tiempo real.

## Mejoras futuras

- Implementar Arduino o ESP32.
- Registrar datos históricos.
- Incorporar monitoreo remoto.
- Implementar alertas.
- Agregar más sensores ambientales.

## Herramientas utilizadas

- Proteus
- Multímetro
- Componentes electrónicos físicos

## Sistema de iluminación

La iluminación fue diseñada utilizando una LDR para detectar el nivel de luz ambiental.

La señal de la LDR era procesada mediante un comparador LM393.

Cuando la iluminación descendía por debajo del umbral configurado, el comparador activaba un relé.

El relé permitía conectar una fuente externa de 12V encargada de alimentar el sistema de LEDs.

Esta configuración permitió controlar cargas de mayor voltaje sin afectar directamente la electrónica de control.

## Evidencia del proyecto

### Imagenes de la maqueta y circuito

![Vista general](01_FOTOS)

