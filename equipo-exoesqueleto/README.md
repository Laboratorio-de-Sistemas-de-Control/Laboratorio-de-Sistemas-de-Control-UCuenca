# Exoesqueleto ALLEX-2 (uso restringido)

> **Este equipo no está disponible para el uso de los estudiantes.** Solo lo opera personal autorizado, con el responsable presente. El manual es una **versión preliminar** que describe el uso hasta noviembre de 2026.

El **ALLEX-2** es un exoesqueleto de extremidades inferiores para uso en el laboratorio. **No es portable:** no está diseñado para que una persona lo lleve puesto. Forma parte de un proyecto de investigación de **gemelo digital**: un modelo matemático identificado, un software de control por capas y simuladores que reflejen el comportamiento del equipo real. Tiene seis articulaciones motorizadas (cadera, rodilla y tobillo en cada pierna).

## Documentos en este repositorio

| Prioridad | Documento | Para qué sirve |
|---|---|---|
| 1 | [01_Manual_de_uso_Exoesqueleto_ALLEX2_preliminar.pdf](Docs/01_Manual_de_uso_Exoesqueleto_ALLEX2_preliminar.pdf) | Manual de uso preliminar (en español, 12 páginas): descripción del sistema, operación actual, estado de las pruebas, restricciones vigentes y pendientes. |

## Datos del equipo

| Característica | Valor |
|---|---|
| Motores | Maxon sin escobillas (EC 90 flat en la cadera y EC 45 flat en rodilla y tobillo) con reductores armónicos |
| Drivers | Maxon EPOS4, uno por articulación, por bus CAN a 500 kbps |
| Control | Raspberry Pi de control y Raspberry Pi 4 con pantalla táctil (interfaz ExoHMI) |
| Modo actual | Control por posición (SDO) |

⚠️ **Por confirmar:** ubicación en el laboratorio y persona responsable.

## Seguridad

- **Solo personal autorizado**, con el responsable presente.
- **Nunca** coloques a una persona en el exoesqueleto ni te acerques a las articulaciones habilitadas.
- Mantén el área despejada y el **paro de emergencia** a la vista.
- Hay observaciones mecánicas pendientes en dos articulaciones: no habilites el equipo sin autorización del responsable.
