# Sistema Multitanque

El **Sistema Multitanque (SMT)** es un banco de pruebas para estudiar el control de **nivel y caudal** de un líquido. Está formado por dos tanques en cascada (la salida del tanque 1 es la entrada del tanque 2), un tanque de bombeo, una bomba y varias válvulas. Se usa en las prácticas de identificación y de control de la asignatura de Control Digital.

## Documentos en este repositorio

Ordenados por prioridad: léelos en este orden.

| Prioridad | Documento | Para qué sirve |
|---|---|---|
| 1 | [01_Manual_de_uso_Sistema_Multitanque.pdf](Docs/01_Manual_de_uso_Sistema_Multitanque.pdf) | Manual de uso del laboratorio (en español, 11 páginas): cómo funciona, componentes, panel de control, variables OPC UA, simulador, mantenimiento y problemas frecuentes. **Empieza por aquí.** |

La guía de la práctica con el sistema multitanque está en el repositorio público de la asignatura: [edu-control-digital](https://github.com/Laboratorio-de-Sistemas-de-Control/edu-control-digital) (carpeta `3_Práctica_SMT`).

## Formas de usarlo

| Forma | Descripción |
|---|---|
| **Banco real** | El equipo físico del laboratorio, con su panel de control, sus PLC y su servidor OPC UA. |
| **Experimentos remotos** | La plataforma web del laboratorio permite enviar experimentos al sistema real. |
| **Simulador** | Un gemelo virtual con el simulador *Tankatwin*, controlado desde Python. Es la forma que se usa en las prácticas de Control Digital. |

## Datos del equipo

| Característica | Valor |
|---|---|
| Cantidad en el laboratorio | 1 |
| Proceso | Dos tanques en cascada y un tanque de bombeo |
| Bomba | Favson F3012, 12 V, 4 L/min |
| Sensores | Ultrasónico HC-SR04 (nivel) y sensor de flujo (caudal) |
| Válvulas | Proporcional, de bola y solenoide |
| Controladores | PLC Siemens S7-1500 y PLC Controllino Maxi, con HMI Siemens KTP 700 |
| Comunicación | OPC UA |

La descripción detallada de los componentes sigue el manual de referencia de la maqueta; la configuración actual puede diferir en algunos componentes.

⚠️ **Por confirmar:** ubicación en el laboratorio y persona responsable del equipo.

## Seguridad

- El banco tiene **agua, bomba, válvulas y equipo eléctrico**: evita derrames sobre las partes eléctricas y no manipules el cableado con el sistema energizado.
- **No operes el banco sin autorización** del personal del laboratorio.
- Conoce el pulsador de **STOP** antes de empezar.
- Ante una fuga o una alarma, detén el sistema y avisa al personal técnico.
