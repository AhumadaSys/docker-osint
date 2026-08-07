# OSINT Docker Lab

## Descripción

Este proyecto tiene como objetivo crear un laboratorio de **OSINT (Open Source Intelligence)** basado en Docker, donde las herramientas se encuentran organizadas por categorías en lugar de concentrarse en una única imagen.

Cada categoría posee su propio `Dockerfile`, lo que permite mantener imágenes pequeñas, independientes y fáciles de actualizar.

La idea es disponer de un entorno modular para investigaciones OSINT, facilitando el mantenimiento y evitando conflictos entre dependencias de distintas herramientas.

---

## Objetivos

* Organizar herramientas OSINT por categorías.
* Mantener imágenes Docker independientes.
* Reducir el tamaño y las dependencias de cada imagen.
* Facilitar la incorporación de nuevas herramientas.
* Disponer de un laboratorio reproducible y portable.

---

## Estructura del proyecto

```text
.
├── metadata
│   ├── data
│   ├── Dockerfile
│   └── README.md
├── osint-phone
│   ├── phoneinfoga
│   │   ├── Dockerfile
│   │   └── README.me
│   └── phonextract
│       ├── dockerfile
│       └── README.me
├── README.md
└── social
    ├── Dockerfile
    └── README.me

7 directories, 9 files
```

Cada directorio representa una imagen Docker independiente con herramientas especializadas para una determinada categoría de OSINT.

---

## Filosofía del proyecto

En lugar de crear una única imagen con decenas de herramientas, este laboratorio adopta una arquitectura modular.

Esto permite:

* Mantener imágenes más livianas.
* Evitar dependencias innecesarias.
* Actualizar cada categoría de forma independiente.
* Comprender mejor qué herramientas pertenecen a cada área de OSINT.

---

## Licencia

Este proyecto se distribuye únicamente con fines educativos y de investigación en seguridad informática.

