---
trigger: always_on
---

# Reglas de Gobernanza: DigiSite ES

## 1. Flujo de Trabajo Obligatorio
- **Spec First:** No se permite escribir código sin una Spec aprobada en `/specs/tasks/`.
- **Trazabilidad:** Cada commit y PR debe referenciar el ID de la Spec (ej. `feat: implement taxonomy based on Spec-001`).

## 2. Estándares de Backend (NestJS)
- Todos los servicios de IA deben residir en el `LlmModule`.
- Las tareas pesadas (Deep Research, parsing de archivos) DEBEN usar `BullMQ`.
- Los endpoints de `/api/v1/` deben estar protegidos por el middleware de `ApiKeyAuth` o `BearerAuth`.

## 3. Seguridad y Secretos
- **HMAC:** Todas las notificaciones de webhooks deben incluir el header `X-DigiSite-Signature`.
- Prohibido subir `credentials.json` o archivos `.env` al repositorio.
- Los secretos deben consultarse a través de la integración de Google Cloud si están configurados.

## 4. Integración de IA
- El sistema no debe usar listas estáticas de modelos. 
- Consultar siempre el endpoint dinámico `GET /llm/available-models` para poblar selectores en la UI.