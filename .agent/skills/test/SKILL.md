---
name: test
description: >
  Genera casos de prueba unitarios y de integración para asegurar que el código 
  cumple con los criterios de aceptación de la spec.
---

# Skill: Testing & Validation

## Proceso
1. **Analizar Criterios de Aceptación:** Lee la sección de "Criterios de Aceptación" de la spec asociada.
2. **Cobertura:**
   - Crear tests para el "Happy Path".
   - Crear tests para casos borde y manejo de errores (ej. 4xx, 5xx).
3. **Frameworks:** Usa Jest para NestJS y Vitest/Cypress para Next.js.

## Formato de Salida
Genera el archivo `.spec.ts` o `.test.tsx` junto al archivo de implementación.