---
name: digisite-branding
description: >
  Aplica la identidad visual oficial de DigiSite ES (Executive Strategy) a cualquier 
  artefacto, código o diseño. Úsala para asegurar coherencia en colores, tipografía 
  y estándares de diseño corporativo en el frontend y documentos.
---

# DigiSite ES Brand Styling

## Resumen

Esta skill proporciona acceso a los recursos de identidad y estilo de DigiSite IA Intelligence & Automation[cite: 6]. Su objetivo es reflejar la insignia "ES Executive Strategy" en cada desarrollo[cite: 7].

**Keywords**: branding, identidad corporativa, DigiSite ES, Executive Strategy, Tailwind CSS, Sora, IBM Plex Sans, paleta de colores, diseño visual.

## Brand Guidelines

### Colores (Paleta Global) [cite: 9]

**Colores Principales:**
- **Cobalt**: `#0047AB` - Color primario de marca.
- **Electric**: `#3A5AFF` - Color secundario para estados activos.
- **Neon Cyan**: `#00F0FF` - Acentos vibrantes y elementos de IA.

**Interfaz y Fondos:**
- **Dark Mode**: Implementación nativa mediante clases `dark:` de Tailwind[cite: 10].
- **Contraste**: Las etiquetas y textos deben mantener legibilidad estricta sobre fondos oscuros[cite: 128].

### Tipografía [cite: 8]

- **Títulos (Headings)**: `Sora` - Para una estética moderna y tecnológica.
- **Cuerpo (Body Text)**: `IBM Plex Sans` - Para máxima legibilidad en reportes y datos.
- **Nota**: En la interfaz web, estas fuentes deben cargarse preferiblemente desde Google Fonts o localmente.

## Características de Aplicación

### Aplicación Inteligente en UI [cite: 11]
- Aplica la fuente **Sora** a todos los elementos `h1` a `h6`[cite: 8].
- Usa **IBM Plex Sans** para párrafos, tablas y entradas de datos[cite: 8].
- Implementa estados visuales (Taxonomía) usando los 10 colores predefinidos de marca para categorías y estados[cite: 26, 78].

### Estilo de Texto y Componentes
- Todos los términos y etiquetas deben estar estrictamente en **Castellano**[cite: 37, 130].
- Los componentes deben soportar **Dark Mode** de forma nativa[cite: 10].
- Los botones y elementos interactivos deben usar transiciones entre **Cobalt** y **Electric**[cite: 9].

### Insignia de Marca
- Cualquier componente de encabezado o pie de página debe incluir la insignia **"ES Executive Strategy"** junto al logo de DigiSite[cite: 7, 131].

## Detalles Técnicos

### Gestión en Frontend (Next.js/Tailwind) [cite: 11, 339]
- Configurar `tailwind.config.js` para incluir los colores `cobalt`, `electric` y `neon-cyan` como variables extendidas[cite: 9].
- Utilizar fuentes variables para optimizar la carga de Sora y IBM Plex Sans[cite: 8].

### Verificación de Calidad [cite: 125]
- Validar contraste de etiquetas en Dark Mode antes de finalizar la tarea[cite: 128].
- Asegurar que no existan términos en inglés en la interfaz visual[cite: 130].