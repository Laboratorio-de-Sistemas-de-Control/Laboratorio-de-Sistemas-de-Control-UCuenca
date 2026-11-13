# Fresadora de PCB Prometheus (Zippy Robotics)

La "CNC" del laboratorio es una **fresadora de circuitos impresos (PCB)** modelo **Prometheus**, de Zippy Robotics. Sirve para fabricar placas
de cobre (fresado de pistas, taladrado y corte del contorno) a partir de archivos Gerber. **No es una fresadora de uso general:** no
mecaniza piezas ni moldes.

## Enlaces oficiales

- **Página oficial de descargas (manual, software ProCAM y videos):** <https://www.zippyrobotics.com/download/>
- Tienda de brocas (solo sirven las brocas de Zippy): <https://shop.zippyrobotics.com>

## Documentos en este repositorio

Ordenados por prioridad: léelos en este orden.

| Prioridad | Documento | Para qué sirve |
|---|---|---|
| 1 | [01_Manual_de_uso_Prometheus.pdf](Docs/01_Manual_de_uso_Prometheus.pdf) | Manual de uso del laboratorio (en español, 26 páginas): seguridad, puesta en marcha, brocas y palpado, fabricación de una placa de ejemplo, archivos Gerber, mantenimiento y problemas frecuentes. **Empieza por aquí.** |
| 2 | [02_Manual_Prometheus_ZippyRobotics.pdf](Docs/02_Manual_Prometheus_ZippyRobotics.pdf) | Manual oficial del fabricante (en inglés, edición de noviembre de 2021; la versión vigente está en la página oficial). |
| 3 | [03_Tarjeta_de_calibracion.pdf](Docs/03_Tarjeta_de_calibracion.pdf) | Tarjeta de calibración, para imprimir. Solo hace falta si las placas salen con los ángulos torcidos (ver el capítulo de mantenimiento del manual de uso). |

## Datos de la máquina

| Característica | Valor |
|---|---|
| Tipo | Fresadora de PCB de escritorio (fresado, taladrado y corte de contorno) |
| Fabricante / modelo | Zippy Robotics / Prometheus |
| Área máxima de trabajo | 6" × 4" (160 mm × 100 mm, formato Eurocard) |
| Placa de cobre admitida | Exactamente 6" × 4" o 160 mm × 100 mm. Con otro tamaño la herramienta puede chocar con la mesa al palpar. |
| Software | **ProCAM** de Zippy Robotics (Windows). Importa archivos Gerber y controla la máquina. |
| Conexión | USB (plug-and-play, sin controladores adicionales) y cable de corriente; interruptor junto a la entrada de corriente |
| Husillo | Propio de Zippy, con "bit clamp" (sujeción con rodamiento) en vez de pinza tradicional |
| Brocas | **Solo brocas de Zippy Robotics.** Las de otras marcas tienen otro diámetro de vástago y dañan los rodamientos del husillo. |
| Archivos de entrada | Gerber: `.gtl` (capa superior), `.gbl` (inferior), `.drl` (taladros), `.gm1` (contorno) |
| Diseño de la placa | Todo el trazado debe estar en el cuadrante positivo de X/Y y dentro de 6" × 4"; lo que quede fuera se recorta. Probado con Altium, Eagle, KiCad, Ultiboard, DipTrace y Upverter. |

⚠️ **Por confirmar** (no consta en el manual): número de serie, número de inventario, ubicación en el laboratorio, computador donde está
instalado ProCAM y persona responsable del equipo.

## Seguridad

Resumen del manual del fabricante (léelo completo antes de operar la máquina):

- **Polvo:** usa una aspiradora con filtro **HEPA o ULPA** al taladrar y al cortar el contorno. No respires el polvo.
- **Fresado bajo aceite mineral:** se recomienda fresar con una capa de aceite mineral sobre la placa para que el polvo de cobre quede en el aceite.
  Después se limpia con papel y se desecha.
- **Partes móviles:** hay riesgo de **atrapamiento**. Mantén las manos lejos de la broca y del motor del husillo, y también el pelo y la ropa suelta,
  sobre todo del tornillo del eje Z.
- **Protección personal:** usa protección para ojos y oídos al fresar.
- **Emergencia:** si ves algo peligroso, **apaga el interruptor de corriente o desconecta el cable de corriente de inmediato.**
- **Reinicio brusco:** apaga la máquina, cierra ProCAM, desconecta y vuelve a conectar el USB, abre ProCAM y recién entonces enciende la máquina.
  Si no, ProCAM sigue enviando comandos. El orificio de reinicio está sobre el puerto USB.
- **Nunca** fresar, taladrar ni cortar sin el *bit clamp* y su rodamiento puestos, ni sin acoplar el motor (la broca no gira y se rompe).

## Uso básico (resumen)

El procedimiento completo, con capturas, está en el manual. En resumen:

1. Cargar los archivos Gerber en ProCAM (de arriba hacia abajo) y elegir las brocas.
2. Pegar la capa de sacrificio sobre la mesa con cinta de doble cara, sin arrugas, al menos 4 tiras a lo largo.
3. Pegar la placa de cobre de la misma manera. No debe tener juego al presionar las esquinas.
4. Conectar el cable caimán entre la barra de latón de la mesa y la placa, y otro de la broca al carro del eje Z, y **palpar** la superficie.
5. Fresar, con aceite mineral, usando protección de ojos y oídos.
6. Taladrar y, si la placa es de doble cara, voltearla, localizar los agujeros con "Locate Holes", palpar y fresar la otra cara.
7. Cortar el contorno de la placa.

## Lo que no incluye la caja

Aceite mineral, aspiradora con filtro HEPA/ULPA, un destornillador para despegar la placa, alcohol (para soltar la cinta o limpiar) y papel toalla.

## Mantenimiento

- Mantén limpia la barra de latón de la mesa (es el punto de referencia de altura) y que no la cubra cinta ni otros objetos.
- Si la máquina se cambia a otro computador, hay que repetir la calibración por software (si hiciera falta), porque esos datos se guardan en el computador
  y no en la máquina.
