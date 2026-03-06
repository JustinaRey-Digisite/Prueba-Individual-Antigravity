---
name: digisite-frontend
description: >
  Genera interfaces de frontend de grado de producción (Next.js/Tailwind) para el 
  ecosistema DigiSite ES. Se enfoca en la composición espacial, 
  layouts complejos y refinamiento de código. ESTA SKILL NO DEFINE EL BRANDING; 
  debe usarse obligatoriamente junto a @digisite-branding para asegurar la 
  coherencia visual.
---

# DigiSite ES: Frontend & UX Studio

Esta skill guía la creación de interfaces de alta gama para el "Studio" inspirado en manus.im. Su objetivo es la excelencia técnica y funcional, dejando la identidad visual en manos de la skill especializada.

## Inter-conexión de Skills
- **Identidad Visual**: Para colores, tipografías y logos, consulta y aplica estrictamente `@digisite-branding`.
- **Lógica de IA**: Para componentes que interactúan con LLMs, coordina con `@chatgpt-api`.

## Guía de Diseño y Composición

### 1. Enfoque "Executive Strategy"
- **Propósito**: Crear herramientas que faciliten la toma de decisiones estratégicas.
- **Estructura**: Prioriza layouts de panel dividido, modales con scroll lateral y dashboards de métricas avanzados.
- **Composición**: Usa composiciones asimétricas y grids dinámicos que rompan la estética genérica de las plantillas comerciales.

### 2. Estándares de Implementación (Next.js + Tailwind)
- **Componentes**: Crea componentes funcionales y modulares con JavaScript.
- **Interactividad**: Implementa micro-interacciones sutiles para feedback (hovers, transiciones de carga).
- **Composición Espacial**: Usa espacios negativos generosos para reducir la carga cognitiva del usuario ejecutivo.
- **Idioma**: Toda la interfaz, comentarios en código y placeholders deben estar estrictamente en **Castellano**.

### 3. Motion y Profundidad
- Utiliza bibliotecas como Framer Motion para entradas escalonadas de datos.
- Aplica efectos de profundidad (Glassmorphism) y sombras dramáticas para jerarquizar la información crítica, siempre respetando el **Dark Mode** definido en el branding.

## Flujo de Trabajo
1. **Analizar la Spec**: Leer la tarea técnica en `/specs/tasks/`.
2. **Cargar Branding**: Activar `@digisite-branding` para obtener la paleta y fuentes.
3. **Ejecución**: Construir el componente asegurando que la insignia "ES Executive Strategy" esté presente en elementos globales.

## Lo que esta skill NO decide
- Los valores hexadecimales de los colores.
- Los nombres de las familias tipográficas.
- La lógica del servidor o endpoints de la API.