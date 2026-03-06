# Ejemplo: Resumir feedback de usuario

## Contexto
Dado el feedback crudo de un cliente, generar un resumen
claro de no más de 3 oraciones.

## Implementación

```typescript
const summary = await client.chat.completions.create({
  model: process.env.OPENAI_MODEL ?? "gpt-4o",
  messages: [
    {
      role: "system",
      content: "Eres un asistente que resume feedback de clientes de forma clara y concisa.",
    },
    {
      role: "user",
      content: `Resume este feedback en 3 oraciones: ${customerFeedback}`,
    },
  ],
  max_tokens: 300,
  temperature: 0.3,
});
```

## Por qué temperature: 0.3
Los resúmenes deben ser precisos y reproducibles, no creativos.
Una temperatura baja reduce la variabilidad del output.