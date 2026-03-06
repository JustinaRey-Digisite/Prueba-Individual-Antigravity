---
name: debug-skill
description: >
  Análisis y corrección de errores. Usar cuando el código no cumple con la spec
  o se reporta un comportamiento inesperado.
---

# Debug Skill

## Proceso de Diagnóstico
1. **Identificar la Spec**: Localizar la spec que rige la funcionalidad afectada.
2. **Análisis de Logs**: Solicitar logs de BullMQ o de la consola de NestJS.
3. **Contraste**: ¿El error es una desviación de la spec o la spec es ambigua?.

## Acciones de Corrección
- Si es error de código: Proponer el fix siguiendo los principios de la arquitectura.
- Si es ambigüedad: Proponer un ajuste a la spec antes de tocar el código.

## Verificación de Webhooks
Si el error es de integración, verificar la firma HMAC y la lógica de reintento.