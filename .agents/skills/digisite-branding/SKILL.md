---
name: digisite-branding
description: >
  Aplica la identidad visual oficial de DigiSite ES (Executive Strategy) a cualquier artefacto, código o diseño. Úsala para asegurar coherencia en colores, tipografía y estándares de diseño corporativo en el frontend y documentos. Se utiliza si digisite-figma-source falla en obtener el diseño de Figma y se necesita un diseño base.
---

# DigiSite ES Brand Styling

## Resumen

Esta skill proporciona acceso a los recursos de identidad y estilo de DigiSite IA Intelligence & Automation. Su objetivo es reflejar la insignia "ES Executive Strategy" en cada desarrollo.

**Keywords**: branding, identidad corporativa, DigiSite ES, Executive Strategy, Tailwind CSS, Sora, IBM Plex Sans, paleta de colores, diseño visual.

## Design Source

Cuando exista un diseño en Figma para el componente solicitado,
el agente debe consultar la skill `digisite-figma-source`
antes de generar código nuevo.

## Brand Guidelines

### Colores (Paleta Global)

**Colores Principales:**
- **Cobalt**: `#0047AB` - Color primario de marca.
- **Electric**: `#3A5AFF` - Color secundario para estados activos.
- **Neon Cyan**: `#00F0FF` - Acentos vibrantes y elementos de IA.

**Interfaz y Fondos:**
- **Dark Mode**: Implementación nativa mediante clases `dark:` de Tailwind.
- **Contraste**: Las etiquetas y textos deben mantener legibilidad estricta sobre fondos oscuros.

### Tipografía

- **Títulos (Headings)**: `Sora` - Para una estética moderna y tecnológica.
- **Cuerpo (Body Text)**: `IBM Plex Sans` - Para máxima legibilidad en reportes y datos.
- **Nota**: En la interfaz web, estas fuentes deben cargarse preferiblemente desde Google Fonts o localmente.

## Características de Aplicación

### Aplicación Inteligente en UI
- Aplica la fuente **Sora** a todos los elementos `h1` a `h6`.
- Usa **IBM Plex Sans** para párrafos, tablas y entradas de datos.
- Implementa estados visuales (Taxonomía) usando los 10 colores predefinidos de marca para categorías y estados.

### Estilo de Texto y Componentes
- Todos los términos y etiquetas deben estar estrictamente en **Castellano**.
- Los componentes deben soportar **Dark Mode** de forma nativa.
- Los botones y elementos interactivos deben usar transiciones entre **Cobalt** y **Electric**.

### Insignia de Marca
- Cualquier componente de encabezado o pie de página debe incluir la insignia **"ES Executive Strategy"** junto al logo de DigiSite.

## Detalles Técnicos

### Gestión en Frontend (Next.js/Tailwind)
- Configurar `tailwind.config.js` para incluir los colores `cobalt`, `electric` y `neon-cyan` como variables extendidas.
- Utilizar fuentes variables para optimizar la carga de Sora y IBM Plex Sans.

### Verificación de Calidad
- Validar contraste de etiquetas en Dark Mode antes de finalizar la tarea.
- Asegurar que no existan términos en inglés en la interfaz visual.