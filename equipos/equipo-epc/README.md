# Entrenador de Planta de Control (EPC)

El **EPC** (modelo EPC-V3, de DataLights) es una placa electrónica didáctica con sensores y actuadores típicos de los sistemas de instrumentación y control: un **LED de temperatura** con su sensor y un ventilador, un **motor DC** con encoder, un **motor paso a paso** con encoder, un **micrófono** y un **relé**. Se conecta a una tarjeta de adquisición de datos (DAQ) de National Instruments, como la NI myDAQ, y se opera con programas de LabVIEW.

Permite hacer prácticas de medición y control de temperatura (On/Off, PWM y PID), de velocidad de un motor DC, de posición de un motor paso a paso, de análisis de sonido y de conmutación de un relé.

## Documentos en este repositorio

Ordenados por prioridad: léelos en este orden.

| Prioridad | Documento | Para qué sirve |
|---|---|---|
| 1 | [01_Manual_de_uso_EPC.pdf](Docs/01_Manual_de_uso_EPC.pdf) | Manual de uso del laboratorio (en español, 13 páginas): partes y terminales, conexión a la DAQ, seguridad, lista de prácticas, sintonía PID y problemas frecuentes. **Empieza por aquí.** |
| 2 | [02_Manual_del_fabricante_EPC_DataLights.pdf](Docs/02_Manual_del_fabricante_EPC_DataLights.pdf) | Manual del fabricante (en español, 80 páginas): procedimiento paso a paso de las 16 prácticas y especificaciones. |

## Datos del equipo

| Característica | Valor |
|---|---|
| Cantidad en el laboratorio | 7 (según el inventario) |
| Fabricante / modelo | DataLights / EPC-V3 |
| Alimentación | Fuente de 12 V DC, 1200 mA |
| Señales | 0 a 5 V, compatibles TTL y LVTTL |
| Requiere | Tarjeta DAQ de National Instruments (en los ejemplos, NI myDAQ), LabVIEW 2015 o superior con el *toolkit* de control PID, y un computador con Windows |
| Prácticas | 16: temperatura (6), velocidad (5), posición (2), sonido (2) y relé (1) |

⚠️ **Por confirmar:** ubicación en el laboratorio, persona responsable y dónde están los programas de LabVIEW (archivos `.vi`) de las prácticas.

## Seguridad

- El **LED de temperatura** se calienta mucho y puede causar quemaduras: mantén la tapa de acrílico colocada y asegurada, y no toques el LED. No mantengas la temperatura sobre 70 °C más de 2 minutos.
- Las bobinas del motor paso a paso también se calientan si quedan energizadas.
- Conecta y desconecta los cables **con la fuente desconectada**.
- Detén los programas con su botón **STOP**, nunca con el botón de abortar de LabVIEW: así se apagan el LED, el ventilador y el motor.
- No conmutes con el relé cargas de más de 1 A.
