---
name: digisite-figma-source
description: >
  Obtiene información de diseño desde archivos de Figma para generar 
  interfaces que respeten el layout, spacing, componentes y tokens definidos 
  en el proyecto de diseño de DigiSite.
---

# Figma Design Extraction

## Purpose

Esta skill se utiliza cuando el agente detecta:

- un enlace de Figma
- un archivo o proyecto de Figma
- un MCP o API conectado a Figma

El objetivo es traducir el diseño de Figma a una estructura que pueda ser utilizada para generar componentes frontend.

## Rules

- Extraer layout, spacing, jerarquía visual y componentes.
- Identificar componentes reutilizables.
- Detectar tokens de diseño (colores, tipografía, tamaños).

## Output

La información extraída debe transformarse en:

- estructura de componentes React
- layout responsive
- tokens compatibles con Tailwind

## Fallback Rules

Si el agente no puede obtener información analizable desde el archivo o proyecto de Figma indicado (por ejemplo: enlace inválido, acceso restringido, error del conector o ausencia de nodos identificables), debe seguir las siguientes reglas estrictas:

1. **No inventar diseños**
   - El agente no debe generar layouts, componentes ni decisiones de diseño por cuenta propia.

2. **Solicitar información adicional**
   - Pedir al usuario o desarrollador uno de los siguientes elementos:
     - un enlace válido de Figma
     - un `node-id` específico
     - capturas de pantalla del diseño
     - una especificación escrita del componente

3. **Limitar la salida**
   - En caso de no disponer de diseño válido, el agente puede:
     - generar únicamente la **estructura técnica mínima del componente**
     - incluir comentarios indicando que el diseño debe completarse cuando Figma esté disponible.

4. **Respetar branding base**
   - Si se necesita crear una estructura mínima, aplicar únicamente las reglas definidas en la skill `digisite-branding` sin introducir decisiones visuales adicionales.

5. **Bloqueo de decisiones de diseño**
   - El agente no debe definir:
     - layouts
     - jerarquía visual
     - tamaños de componentes
     - spacing
     - estilos de interacción