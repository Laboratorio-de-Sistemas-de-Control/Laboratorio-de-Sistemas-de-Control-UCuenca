# Impresora 3D Robo R2 (Robo 3D)

La impresora 3D del laboratorio es una **Robo R2**, de Robo 3D. Es una impresora **FDM** (modelado por deposición fundida): funde filamento
plástico y construye la pieza capa por capa. Se usa para fabricar piezas, carcasas y prototipos.

## Documentos en este repositorio

Ordenados por prioridad: léelos en este orden.

| Prioridad | Documento | Para qué sirve |
|---|---|---|
| 1 | [01_Manual_de_uso_Robo_R2.pdf](Docs/01_Manual_de_uso_Robo_R2.pdf) | Manual de uso del laboratorio (en español, 21 páginas): seguridad, puesta en marcha, calibración, impresión de una pieza, control remoto y mantenimiento. **Empieza por aquí.** |
| 2 | [02_Manual_fabricante_Robo.pdf](Docs/02_Manual_fabricante_Robo.pdf) | Manual oficial del fabricante, "Robo User Manuals" (en inglés, 202 páginas, edición de mayo de 2018). Consúltalo para el detalle; el capítulo 6 es el de la R2. |

## Ejemplo para practicar

| Archivo | Para qué sirve |
|---|---|
| [Final Eiffel Tower.STL](Ejemplos/Final%20Eiffel%20Tower.STL) | Modelo 3D de ejemplo para practicar el laminado en Cura for Robo y la primera impresión. |

## Datos de la máquina

| Característica | Valor |
|---|---|
| Cantidad en el laboratorio | 2 impresoras |
| Tipo | Impresora 3D FDM de escritorio |
| Fabricante / modelo | Robo 3D / Robo R2 |
| Control | Pantalla táctil a color (RoboOS) con tres pestañas: *Files*, *Printer* y *Utilities* |
| Conexión | Wi-Fi o cable Ethernet, memoria USB y modo *hotspot*. También se controla desde un panel web y desde la app Robo (iOS). |
| Cámara | Cámara integrada (solo la R2), apagada por defecto, con opción de *timelapse* |
| Software de laminado | **Cura for Robo** (Windows de 64 bits y tarjeta gráfica compatible con OpenGL 2) |
| Archivos | Modelo `.stl` → laminado a `.gcode` → impresión desde la pantalla, una USB o el panel web |
| Alimentación | Fuente externa de 24 V |
| Temperatura máxima | Hotend, unos 300 °C. Cama, unos 110 °C. |
| Superficie de impresión | Lámina PEI magnética y removible |
| Filamento | PLA y ABS |

⚠️ **Por confirmar** (no consta en los manuales): número de serie, número de inventario, ubicación en el laboratorio,
volumen de impresión y persona responsable del equipo.

### Temperaturas de referencia

| Material | Hotend | Cama (R2) |
|---|---|---|
| PLA | 190 °C – 210 °C | 50 °C (hasta 70 °C) |
| ABS | 230 °C – 250 °C | 80 °C (hasta 100 °C) |

Para el filamento Robo, 190 °C es el valor óptimo de PLA y 230 °C el de ABS.

## Seguridad

Resumen del manual (léelo completo antes de usar la impresora):

- **Quemaduras:** el hotend llega a unos 300 °C y la cama a unos 110 °C. No toques el hotend con las manos: usa las pinzas y espera al menos
  30 minutos a que se enfríe.
- **Partes móviles:** no metas la mano ni objetos dentro de la impresora cuando esté en marcha, a punto de arrancar o en reposo.
- **Supervisión:** no la dejes sola durante una impresión, vigila la primera capa y apágala al terminar.
- **Electricidad:** usa solo el cable original, con buena conexión a tierra. Todo mantenimiento se hace con la impresora **apagada y desenchufada**.
  No modifiques la electrónica.
- **Ventilación:** el plástico fundido emite olor; trabaja en un lugar ventilado y sin comida ni bebida cerca.
- **Piezas y herramientas:** usa guantes al retirar las piezas y las herramientas solo para su fin. Mantén el equipo lejos de líquidos, fuentes de calor y niños.
- **Emergencia** (recomendación general; no viene en el manual): si ves algo peligroso (humo, olor a quemado, cortocircuito), apaga la impresora y desconecta el cable de corriente.

## Uso básico (resumen)

El procedimiento completo, con capturas, está en el manual de uso. En resumen:

1. **Antes de empezar:** verifica que la cama esté libre, que nada impida el movimiento del cabezal y que no queden trozos de filamento en el extrusor.
2. **Calibrar el Z-Offset:** *Utilities → Wizards → Z-Offset Wizard*, deslizando la tarjeta de calibración (o una hoja de papel) entre la boquilla y la cama.
   Es la causa principal de una buena primera capa. Antes del ajuste fino, nivela la cama con los tornillos de mariposa.
3. **Cargar filamento:** *Utilities → Wizards → Filament Loading Wizard*. El filamento debe pasar por el bloque del sensor.
4. **Laminar:** abre el `.stl` en Cura for Robo, elige el mismo material que está cargado y un perfil (*Low*, *Medium*, *High* o *Ultra High*), revisa
   las capas y exporta el `.gcode`.
5. **Imprimir:** desde *Files* (memoria interna o USB) pulsa *Start*, o sube el archivo al panel web.
6. **Vigilar la primera capa.** Si la boquilla arrastra o el plástico no se pega, cancela y repite la calibración.
7. **Retirar la pieza:** espera a que se enfríen la pieza y la cama, saca la cama con las dos manos y levanta la pieza por los bordes con la espátula.
   Limpia la lámina PEI con un paño húmedo.

**Cambio de material:** si pasas de ABS a PLA, calienta el hotend a la temperatura de ABS y empuja un poco de PLA para sacar todo el ABS.
Después baja a la temperatura del PLA; si no, la boquilla puede taparse.

## Mantenimiento

| Tarea | Frecuencia |
|---|---|
| Revisar cama libre, cables recogidos y software actualizado | Antes de cada impresión |
| Aceite 3 en 1 en los bujes lisos de los soportes X e Y | Cada 2 a 4 meses |
| Limpiar el engranaje alimentador y lubricar con grasa blanca de litio las varillas del cabezal y el husillo del eje Z | Cada 6 a 12 meses, según el uso |
| Lijar la lámina PEI con lija de grano 2000 si las piezas ya no se pegan, y repetir el Z-Offset | Cada 4 a 6 meses aproximadamente |
| Cambiar la boquilla (hotend), con la impresora apagada, desenchufada y el hotend frío | Cuando haga falta |

## Solución de problemas (los más frecuentes)

| Problema | Qué hacer |
|---|---|
| La pieza no se pega a la cama | Actualizar la impresora, repetir el Z-Offset Wizard y el Fine Tune, limpiar o lijar la PEI y usar *raft* |
| No sale material | Revisar los cables del hotend, limpiar y apretar el engranaje y desenredar el carrete |
| Hotend tapado | Calentar y extraer el filamento con las pinzas y revisar el ventilador del hotend |
| Capas desplazadas | Apretar los tornillos de las poleas y realinear los ejes |
| Error de sensor de filamento | Hacer pasar todo el filamento por el bloque del sensor |

La tabla completa está en el capítulo 5 del manual de uso.
