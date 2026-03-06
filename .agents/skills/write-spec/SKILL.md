---
name: write-spec
description: >
  Guía para escribir specs dentro de un flujo SDD en Antigravity.
  Usar cuando se necesite definir una nueva funcionalidad, modelar
  un caso de uso, o documentar el comportamiento esperado de un
  componente del sistema.
---

# Write Spec Skill

Esta skill guía al agente para redactar specs claras, completas y
compatibles con el flujo de Spec-Driven Development de Antigravity.

## Cuándo usar esta skill

- Se va a desarrollar una funcionalidad nueva
- Se necesita documentar el comportamiento esperado de un componente
- Se está refinando o revisando una spec existente
- El equipo necesita alinear criterios antes de comenzar la implementación

## Estructura de una spec

Toda spec debe incluir las siguientes secciones:

**1. Encabezado**
- `spec_name`: nombre único en kebab-case
- `version`: número de versión (empezar en 1.0)
- `description`: qué problema resuelve esta spec

**2. Input**
- Qué datos recibe el agente o sistema
- Tipos de datos esperados
- Cuáles son obligatorios y cuáles opcionales

**3. Output esperado**
- Forma y tipo del resultado
- Restricciones de formato (longitud, idioma, estructura)

**4. Criterios de aceptación**
- Condiciones que deben cumplirse para considerar la spec satisfecha
- Casos borde a contemplar

## Convenciones a seguir

- Los nombres de specs van en kebab-case: `summarize-feedback`, `validate-input`
- Versionar cada cambio significativo: 1.0 → 1.1 (ajuste menor), 1.0 → 2.0 (cambio de contrato)
- Una spec describe QUÉ se necesita, nunca CÓMO implementarlo
- No mencionar proveedores ni tecnologías concretas dentro de la spec

## Árbol de decisión
```
¿La spec describe una acción sobre datos externos (API, DB)?
  ├── Sí → Definir claramente los inputs que vienen de afuera
  └── No → Enfocarse en el flujo interno del agente

¿El output puede tener más de una forma válida?
  ├── Sí → Listar todas las variantes en "Output esperado"
  └── No → Describir el único formato esperado

¿Hay condiciones de error que el sistema deba manejar?
  ├── Sí → Incluirlas como criterios de aceptación negativos
  └── No → Documentar solo el happy path
```

## Lo que esta skill NO decide

- Qué tecnología o proveedor implementa la capacidad
- Cómo se estructura el código que satisface la spec
- Priorización o secuencia de desarrollo entre specs