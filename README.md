# DigiSite ES · Executive Strategy

Este es el repositorio central del proyecto **DigiSite ES**, basado en una arquitectura robusta de **Spec-Driven Development (SDD)**.

## 🏗️ Arquitectura
- **Backend:** NestJS (ubicado en `apps/api`)
- **Frontend:** Next.js (ubicado en `apps/web`)
- **Gestión de IA:** LlmModule integrado con modelos dinámicos de OpenAI y otros proveedores.

## 📑 Gobernanza y Desarrollo (SDD)
Este proyecto sigue reglas estrictas de desarrollo:
1. **Spec-First:** Todo cambio requiere una especificación previa en `/specs/tasks/`.
2. **Strict Spanish:** Toda la interfaz de usuario debe estar en castellano.
3. **Traceability:** Uso de Conventional Commits referenciando IDs de Specs.

## 🛠️ Estructura del Proyecto
- `apps/`: Contiene las aplicaciones (API y Web).
- `specs/`: Fuente de verdad de todo el negocio y tareas.
- `.agent/`: Configuración del agente Antigravity, reglas y habilidades específicas.
- `libs/`: Librerías y utilidades compartidas.

---

*Desarrollado con Antigravity · Advanced Agentic Coding*
