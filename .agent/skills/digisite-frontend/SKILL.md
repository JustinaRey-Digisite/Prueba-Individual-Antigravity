---
name: digisite-frontend
description: >
  Genera interfaces de frontend de grado de producción (Next.js/Tailwind) para el 
  ecosistema DigiSite ES[cite: 11, 13, 14]. Se enfoca en la composición espacial, 
  layouts complejos y refinamiento de código. ESTA SKILL NO DEFINE EL BRANDING; 
  debe usarse obligatoriamente junto a @digisite-branding para asegurar la 
  coherencia visual.
---

# DigiSite ES: Frontend & UX Studio

Esta skill guía la creación de interfaces de alta gama para el "Studio" inspirado en manus.im[cite: 14, 31]. Su objetivo es la excelencia técnica y funcional, dejando la identidad visual en manos de la skill especializada.

## Inter-conexión de Skills
- **Identidad Visual**: Para colores, tipografías y logos, consulta y aplica estrictamente `@digisite-branding`[cite: 6, 8, 9].
- **Lógica de IA**: Para componentes que interactúan con LLMs, coordina con `@chatgpt-api`.

## Guía de Diseño y Composición

### 1. Enfoque "Executive Strategy"
- **Propósito**: Crear herramientas que faciliten la toma de decisiones estratégicas[cite: 4, 140].
- **Estructura**: Prioriza layouts de panel dividido, modales con scroll lateral y dashboards de métricas avanzados[cite: 38, 101, 102].
- **Composición**: Usa composiciones asimétricas y grids dinámicos que rompan la estética genérica de las plantillas comerciales.

### 2. Estándares de Implementación (Next.js + Tailwind) [cite: 11, 339]
- **Componentes**: Crea componentes funcionales, modulares y altamente tipados con TypeScript.
- **Interactividad**: Implementa micro-interacciones sutiles para feedback (hovers, transiciones de carga)[cite: 89].
- **Composición Espacial**: Usa espacios negativos generosos para reducir la carga cognitiva del usuario ejecutivo.
- **Idioma**: Toda la interfaz, comentarios en código y placeholders deben estar estrictamente en **Castellano**[cite: 37, 130].

### 3. Motion y Profundidad
- Utiliza bibliotecas como Framer Motion para entradas escalonadas de datos.
- Aplica efectos de profundidad (Glassmorphism) y sombras dramáticas para jerarquizar la información crítica, siempre respetando el **Dark Mode** definido en el branding[cite: 10, 128].

## Flujo de Trabajo
1. **Analizar la Spec**: Leer la tarea técnica en `/specs/tasks/`[cite: 20].
2. **Cargar Branding**: Activar `@digisite-branding` para obtener la paleta y fuentes[cite: 5, 8, 9].
3. **Ejecución**: Construir el componente asegurando que la insignia "ES Executive Strategy" esté presente en elementos globales[cite: 7, 131].

## Lo que esta skill NO decide
- Los valores hexadecimales de los colores[cite: 9].
- Los nombres de las familias tipográficas[cite: 8].
- La lógica del servidor o endpoints de la API[cite: 135, 197].