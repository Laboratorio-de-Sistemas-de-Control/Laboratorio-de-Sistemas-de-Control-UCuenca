# Tableros de control (Controllino Mega y ESP32 PLC 14)

El **tablero de control** es un equipo didáctico que integra dos PLC de grado industrial, el **Controllino Mega** y el **ESP32 PLC 14**, con una pantalla táctil (HMI), borneras, LED, botones, un *switch* de red y *protoboards*. Se programan desde Arduino IDE. Se usan en las prácticas de automatización de la asignatura de Control Digital.

## Documentos en este repositorio

Ordenados por prioridad: léelos en este orden.

| Prioridad | Documento | Para qué sirve |
|---|---|---|
| 1 | [01_Manual_de_uso_Tableros_Control.pdf](Docs/01_Manual_de_uso_Tableros_Control.pdf) | Manual de uso del laboratorio (en español, 17 páginas): componentes, encendido, programación, carga de la interfaz del HMI, comunicación HMI–Controllino y problemas frecuentes. **Empieza por aquí.** |

Las prácticas que usan estos tableros están en el repositorio público de la asignatura: [edu-control-digital](https://github.com/Laboratorio-de-Sistemas-de-Control/edu-control-digital) (carpeta `1_Tableros de Control`). Material del HMI Stone: [HMI-Stone](https://github.com/HenryM19/HMI-Stone).

## Versiones

| Versión | HMI |
|---|---|
| Tablero V1 | Stone STWC050WT-01 (5 pulgadas) |
| Tablero V2 | Coolmay TK6070FH (7 pulgadas) |

## Datos del equipo

| Característica | Valor |
|---|---|
| Controladores | Controllino Mega y ESP32 PLC 14 (con RS485, Ethernet, WiFi y LoRa) |
| Alimentación de las borneras | 24 V DC (fuente AC/DC del tablero) |
| Puertos de 5 V | `X1` a `X4` del Controllino Mega |
| Programación | Arduino IDE |
| Comunicación con el HMI | Serial (Stone) y Modbus RTU por RS485 (Coolmay) |

⚠️ **Por confirmar:** número de tableros, ubicación en el laboratorio y persona responsable.

## Seguridad

- Las borneras operan a **24 V DC**. Haz los cambios de cableado con el tablero **apagado y desconectado**.
- Los puertos `X1` a `X4` del Controllino operan a **5 V**: no los mezcles con las borneras de 24 V.
- No conectes cargas distintas a las previstas para las prácticas sin consultar al personal del laboratorio.
