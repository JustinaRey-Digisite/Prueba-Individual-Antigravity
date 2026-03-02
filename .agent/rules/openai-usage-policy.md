---
trigger: always_on
---

# Política de uso de OpenAI (ChatGPT)

1. [cite_start]**Uso Obligatorio de Skill**: Toda implementación que use OpenAI debe seguir las instrucciones de la skill `chatgpt-api`.
2. **Seguridad**: Prohibido hardcodear `OPENAI_API_KEY`. [cite_start]Usar siempre variables de entorno.
3. [cite_start]**Consumo Dinámico**: El modelo (`model`) debe leerse de la variable `OPENAI_MODEL` o del endpoint `/llm/available-models` de DigiSite[cite: 2].
4. [cite_start]**Traducción**: El backend debe mapear los nombres de modelos y respuestas al castellano antes de enviarlos al frontend[cite: 2].
5. [cite_start]**Manejo de Costos**: Cada llamada a la API debe registrarse en el `LlmLog` de la base de datos para el Dashboard de métricas[cite: 2].