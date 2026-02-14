# Requerimientos del Sistema — Alcance (scope.md)

> Ruta: DOSW-Laboratorio4/docs/requirements/scope.md

## 1. Sistema

- **Nombre del sistema:** DOSW-Laboratorio4
- **Objetivo:** El sistema tiene como objetivo proporcionar los artefactos y ejecuciones necesarias para el laboratorio 4, permitiendo compilar, ejecutar y probar la aplicación Java del curso, además de centralizar la documentación y evidencias del equipo.

## 2. Problema a resolver

Describir el problema principal a resolver por este sistema. Por ejemplo:

- El repositorio y la aplicación carecen de una estructura uniforme para la documentación, evidencias y ejecución de pruebas; se requiere un sistema que organice, ejecute y entregue resultados reproducibles para el laboratorio.

## 3. Diagrama de contexto

### 3.1 Diagrama

Incluya aquí la imagen del diagrama de contexto realizado (copiar el archivo a `docs/uml/` y usar el nombre `contexto.png` o `contexto.pdf`).

- Imagen sugerida: `docs/uml/contexto.png`

### 3.2 Actores

| Actor / Rol | Descripción |
|-------------|-------------|
| Usuario final | Usuario que compila, ejecuta y prueba la aplicación (estudiante). |
| Administrador / Profesor | Usuario que revisa evidencias, califica y gestiona el repositorio. |

### 3.3 Sistemas externos

| Sistema | Descripción |
|--------:|-------------|
| Repositorio GitHub | Aloja el código fuente y los artefactos del proyecto. |
| Servicio de CI (opcional) | Ejecuta compilaciones y pruebas de forma automatizada. |
| Sistema de Reportes | Genera reportes o exporta resultados de pruebas (CSV/PDF). |

## 4. Alcance del sistema

### 4.1 Dentro del sistema (Funciones que el sistema SÍ realiza — relacione al menos 4)

1. Organizar la estructura del repositorio (`src/`, `docs/`, `pom.xml`).
2. Compilar el proyecto Java mediante Maven (`mvn package`).
3. Ejecutar pruebas unitarias y mostrar resultados (`mvn test`).
4. Almacenar documentación y evidencias en `docs/` (diagramas, capturas, requisitos).

### 4.2 Fuera del sistema (Funciones que NO realiza — relacione al menos 3)

1. No administra la infraestructura de despliegue en la nube.
2. No procesa pagos ni integra pasarelas financieras.
3. No realiza envíos masivos de correo (solo pueden configurarse hooks externos).

---

**Autor:** Equipo DOSW
**Fecha:** 2026-02-14

> Notas:
> - Reemplace las secciones con información específica del caso de estudio si aplica.
> - Para el Diagrama de Contexto copie la imagen a `docs/uml/contexto.png` y actualice este documento con el enlace/imagen.
