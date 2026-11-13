# Laboratorio de Sistemas de Control — Universidad de Cuenca

Información pública del **Laboratorio de Sistemas de Control** de la Universidad de Cuenca: guías y manuales de uso de los equipos, normas del laboratorio y de seguridad, y los formularios para solicitar bienes.

## Qué hay aquí

| Carpeta | Contenido |
|---|---|
| [`equipos/`](equipos/) | Guía de cada equipo: qué es, sus datos, seguridad, y los manuales en PDF. |
| [`normas/`](normas/README.md) | Normas de trabajo, normas de seguridad y protocolo de emergencia (en preparación). |
| [`solicitudes/`](solicitudes/README.md) | Formularios (Acta de entrega de bienes) y cómo solicitar un bien. |

## Equipos disponibles

| Equipo | Para qué sirve | Carpeta |
|---|---|---|
| **Impresora 3D Robo R2** (Robo 3D) | Fabricar piezas, carcasas y prototipos en plástico (FDM) | [equipo-impresoras-3d](equipos/equipo-impresoras-3d/README.md) |
| **Fresadora de PCB Prometheus** (Zippy Robotics) | Fabricar placas de circuito impreso: fresado de pistas, taladrado y corte del contorno | [equipo-cnc](equipos/equipo-cnc/README.md) |
| **Sistema Multitanque** | Identificación y control de nivel y caudal de un líquido (banco real, experimentos remotos y simulador) | [equipo-multitanque](equipos/equipo-multitanque/README.md) |
| **Tableros de control** (Controllino Mega y ESP32 PLC 14) | Prácticas de automatización con PLC y HMI | [equipo-tableros-control](equipos/equipo-tableros-control/README.md) |
| **QUBE-Servo 3** (Quanser) | Control de motor DC, posición y péndulo invertido | [equipo-qube-servo3](equipos/equipo-qube-servo3/README.md) |
| **Robot LEGO MINDSTORMS EV3** | Introducción a la robótica y a la programación | [equipo-lego-ev3](equipos/equipo-lego-ev3/README.md) |
| **Exoesqueleto ALLEX-2** | Investigación (tesis de maestría). **Uso restringido: no disponible para estudiantes** | [equipo-exoesqueleto](equipos/equipo-exoesqueleto/README.md) |

## Cómo está organizado

```text
/
├── equipos/
│   └── equipo-<nombre>/
│       ├── README.md        ← qué es el equipo, datos, seguridad y uso básico
│       ├── Docs/            ← solo documentación: PDF numerados por prioridad (01_..., 02_...)
│       └── Ejemplos/        ← archivos de ejemplo para practicar (solo si el equipo los tiene)
├── normas/                  ← normas de trabajo, de seguridad y de emergencia
└── solicitudes/             ← formularios para solicitar bienes
```

Los PDF de cada equipo van numerados por prioridad: empieza por el `01_`. En el repositorio solo hay documentos finales (PDF, formularios y archivos de ejemplo), no fuentes de edición.

## Antes de usar un equipo

- Lee la sección de **seguridad** del README del equipo y su manual de uso (`01_...`).
- Si no sabes usar un equipo, pide autorización al personal del laboratorio antes de operarlo.
- Para llevar un bien en préstamo, llena el formulario de [solicitudes](solicitudes/README.md).

## Notas

- Los manuales de los fabricantes están en su idioma original. Para la versión más reciente de la fresadora, usa el enlace oficial que aparece en su README.
- Los datos marcados con `⚠️ por confirmar` todavía no están verificados.
- Este repositorio es **público**: no contiene inventarios, registros de mantenimiento ni datos personales. Eso se maneja en un repositorio interno.

## Responsable

Laboratorio de Sistemas de Control — Universidad de Cuenca. *(Completar con la persona de contacto.)*
