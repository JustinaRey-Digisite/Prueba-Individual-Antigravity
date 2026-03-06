---
name: openai-api
description: >
  Provee instrucciones para llamar a la API de OpenAI y generar
  código o texto en lenguaje natural. Usar cuando se necesite integrar generación de
  código, resumir contenido o cualquier tarea que
  requiera un modelo de lenguaje como proveedor externo.
---

# OpenAI API Skill

Esta skill guía al agente para integrar y utilizar la API de OpenAI
dentro del proyecto, siguiendo las convenciones de Antigravity.

## Cuándo usar esta skill

- La tarea requiere generar, resumir o transformar código o texto con un LLM
- Se está implementando o modificando código que llama a la API de OpenAI
- Se necesita configurar parámetros del modelo (temperature, tokens, etc.)

## Configuración requerida

Antes de usar la API, verificar que las siguientes variables de entorno
estén disponibles en el entorno de ejecución. Nunca deben estar
hardcodeadas en el código ni en ningún archivo del repositorio.

| Variable         | Descripción                          | Ejemplo   |
|------------------|--------------------------------------|-----------|
| `OPENAI_API_KEY` | Credencial de autenticación          | `sk-...`  |
| `OPENAI_MODEL`   | Modelo a utilizar                    | `gpt-4o`  |

## Parámetros principales de la API

Al construir una llamada a la API de OpenAI, usar los siguientes
parámetros como punto de partida:

**Obligatorios:**
- `model` → leer desde `OPENAI_MODEL` (nunca hardcodear el modelo)
- `messages` → array con roles `system` y `user`
- `max_tokens` → límite recomendado: 800

**Opcionales pero recomendados:**
- `temperature` → controla creatividad (0.0 a 1.0, default: 0.7)
- `top_p` → control probabilístico alternativo (default: 1)
- `frequency_penalty` → reduce repetición (default: 0)
- `presence_penalty` → fomenta variedad temática (default: 0)

## Manejo de errores

Siempre contemplar los siguientes escenarios al integrar la API:

- **401 Unauthorized** → `OPENAI_API_KEY` inválida o no configurada
- **429 Too Many Requests** → rate limit alcanzado, implementar retry con backoff
- **500/503** → error del lado de OpenAI, reintentar con timeout
- **Respuesta vacía** → `choices[0]?.message?.content` puede ser null, usar fallback

## Lo que esta skill NO decide

Los siguientes aspectos pertenecen a la spec o a la lógica de negocio,
no a esta skill:

- Qué prompt enviar (eso lo define la spec o el agente según el caso de uso)
- Qué hacer con el texto generado
- Si el output cumple los criterios de calidad del producto