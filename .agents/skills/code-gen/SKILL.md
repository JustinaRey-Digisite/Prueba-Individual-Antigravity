---
name: code-gen
description: >
  Genera código (NestJS, Next.js, etc.) basado estrictamente en una especificación (Spec).
  Úsalo cuando se deba implementar una nueva funcionalidad o módulo desde cero.
---

# Skill: Code Generation (SDD)

## Objetivo
Implementar lógica de negocio, controladores, servicios o componentes siguiendo la "Fuente de Verdad" definida en `/specs`.

## Instrucciones de Uso
1. **Revisar el archivo "@/specs/conventions.md"** para conocer las convenciones del proyecto.
2. **Localizar la Spec:** Antes de generar código, busca el archivo `.md` correspondiente en `/specs`.
3. **Alineación Arquitectónica:** 
   - Backend: Sigue el patrón modular de NestJS.
   - Frontend: Usa componentes funcionales de React con Tailwind CSS.
4. **No Inventar:** Si la spec no define un comportamiento, solicita aclaración antes de proponer una implementación.

## Restricciones
- No hardcodear secretos (usar variables de entorno).
- Respetar el tipado estricto de TypeScript.
- Seguir las convenciones de nombres definidas en el proyecto.