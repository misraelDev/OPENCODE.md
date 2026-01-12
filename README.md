# Guía de comandos opencode 📘

Documentación clara y estandarizada para gestionar proyectos con **opencode**, incluyendo navegación, control, agentes y automatización.

---

## Introducción 🚀

Este repositorio contiene la **documentación y configuración oficial** para trabajar con proyectos usando opencode. Su objetivo es facilitar flujos de trabajo consistentes mediante comandos de terminal y agentes de automatización impulsados por ia.

---

## Navegación y gestión de proyectos 🧭

| comando                | descripción                             |
| ---------------------- | --------------------------------------- |
| `cd ruta/del/proyecto` | accede al directorio del proyecto       |
| `opencode`             | abre el proyecto por primera vez        |
| `/init`                | crear planificacion                     |
| `opencode -c`          | reabre el proyecto con la sesión previa |
| `ctrl + c` (2 veces)   | cierra la sesión activa                 |

---

## Comandos de control 🎛️

Atajos útiles para controlar la ejecución dentro de opencode:

| atajo           | acción                                      |
| --------------- | ------------------------------------------- |
| `mayús + !`     | abre la línea de comandos interna           |
| `esc` (2 veces) | interrumpe el proceso o ejecución actual    |
| `/undo + enter` | revierte el proyecto a una versión anterior |

---

## Agentes y automatización 🤖

Opencode permite definir **tareas automatizadas** mediante agentes de ia. Estas tareas se configuran como archivos markdown dentro del directorio:

```
.opencode/command/
```

Cada archivo representa una acción específica que puede ejecutar un agente.

---

### Estructura de archivos en `.opencode/command/` 📁

Ejemplo de archivo: `test.md`

```md
---
description: run tests with coverage
agent: build
model: anthropic/claude-3-5-sonnet-20241022
---

run the full test suite with coverage report and show any failures.
focus on the failing tests and suggest fixes.
```

**Campos clave:**

* **description**: describe brevemente la tarea
* **agent**: tipo de agente que ejecutará la acción
* **model**: modelo de ia utilizado
* **contenido**: instrucciones detalladas para el agente

---

## Recomendaciones ✅

* Mantén los comandos simples y bien descritos
* Usa nombres de archivos claros para cada tarea
* Documenta cualquier cambio en los agentes o flujos

---

*Última actualización: 2026*
