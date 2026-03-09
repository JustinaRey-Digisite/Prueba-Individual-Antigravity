---
name: digisite-development-conventions
type: conventions
scope: global
enforced: true
---

# 📑 Convenciones de Desarrollo · DigiSite ES

Este documento define los **estándares de nomenclatura, estructura y estilo** para el proyecto **DigiSite ES**.

El cumplimiento de estas convenciones es **obligatorio** para garantizar:
- Mantenibilidad del código
- Consistencia entre equipos
- Integración fluida con los agentes de Antigravity
- Correcta aplicación del enfoque **Spec-Driven Development (SDD)**

---

## 1. Nomenclatura (Naming Conventions)

### 1.1 Archivos y Carpetas

- **Carpetas**  
  - Siempre en `kebab-case`  
  - Ejemplos:
    - `presentation-module`
    - `ui-components`

- **Archivos de código**  
  - `kebab-case` + sufijo de tipo  
  - Ejemplos:
    - `auth.service.ts`
    - `button.component.tsx`
    - `feat-taxonomy.spec.md`

- **Specs**
  - Obligatoriamente en `kebab-case`
  - Ubicadas dentro del directorio:
    ```
    /specs/
    ```

---

### 1.2 Código (TypeScript)

- **Clases e Interfaces**
  - `PascalCase`
  - Ejemplos:
    - `PresentationService`
    - `UserInterface`

- **Funciones y Variables**
  - `camelCase`
  - Ejemplos:
    - `calculateLlmCost`
    - `isDeepResearchActive`

- **Constantes y Enums**
  - `UPPER_SNAKE_CASE`
  - Ejemplos:
    - `MAX_TOKENS_LIMIT`
    - `COBALT_COLOR`

- **Base de Datos (Prisma)**
  - Modelos: `PascalCase`
  - Campos: `camelCase`

---

## 2. Estructura del Monorepo

Para mantener una separación clara entre backend y frontend, el proyecto sigue la siguiente jerarquía:

```txt
/
├── apps/
│   ├── api/                # NestJS Backend
│   └── web/                # Next.js Frontend
├── specs/                  # Fuente de verdad (SDD)
│   ├── tasks/              # Specs funcionales
│   └── branding/           # Guías de marca
├── .agents/
│   ├── skills/             # Capacidades de Antigravity
│   └── rules/              # Reglas del workspace
└── libs/                   # Código compartido (Types, Utils)

```

## 3. Estándares de Interfaz y Localización (Strict Spanish)
### 3.1 Idioma de la UI

Todos los textos visibles al usuario deben estar en Castellano, incluyendo:

- Labels
- Placeholders
- Botones
- Mensajes de error
- Mensajes de estado

El uso de términos en inglés en la interfaz está prohibido.

### 3.2 Branding Visual

Seguir las guías de marca definidas en el archivo `@/skills/digisite-branding.md`.

## 4. Flujo de Git y Commits

Se utiliza Conventional Commits para mantener trazabilidad directa con las Specs.

Ejemplos válidos:

- feat(spec-001): nueva taxonomía de estados
- fix(studio): corregir error en generación de slides
- docs(specs): actualizar convenciones de nomenclatura
- refactor(llm): optimizar cálculo de costos sin cambiar funcionalidad

Cada commit debe ser claro, atómico y trazable.

## 5. Reglas de Backend (NestJS + BullMQ)
### 5.1 Procesos Pesados

Cualquier tarea que dure más de 5 segundos debe ejecutarse como un job en BullMQ.

Ejemplos:

- Deep Research
- Parsing de archivos
- Procesamiento multimodal

### 5.2 Logs de IA

Cada llamada a un LLM debe generar un registro en el modelo LlmLog.

El objetivo es permitir:

- Seguimiento de uso
- Cálculo de costos
- Auditoría por presentación y usuario

## 6. Cumplimiento

El incumplimiento de estas convenciones se considera una violación del estándar del proyecto y puede derivar en:

- Rechazo de PR
- Reversión de cambios
- Revisión técnica obligatoria