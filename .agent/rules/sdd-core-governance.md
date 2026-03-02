---
trigger: always_on
---

# DigiSite ES · Regla Central de Desarrollo

Esta regla define las **restricciones obligatorias** para el desarrollo colaborativo y la integridad técnica del proyecto **DigiSite ES**.  
Su cumplimiento es **no negociable** para cualquier implementación realizada en el ecosistema del proyecto.

---

## 1. Ciclo de Vida de Desarrollo (Spec-First)

### 1.1 Verificación de Spec
Antes de implementar cualquier funcionalidad, **debe existir** una especificación aprobada (Spec) en la ruta: @/specs/

No se permite iniciar desarrollo sin una Spec válida.

### 1.2 Fuente de Verdad
- El código **debe ser una implementación fiel** de la Spec correspondiente.
- Si una funcionalidad **no está definida explícitamente** en la Spec:
  - **No debe implementarse**
  - Debe proponerse primero como cambio de Spec

---

## 2. Estándares de Calidad y Testing

### 2.1 Cobertura Obligatoria
Toda función pública creada o modificada **debe contar** con al menos uno de los siguientes:

- Test unitario
- Test de integración

No se aceptan implementaciones sin validación automatizada.

### 2.2 Frameworks Técnicos Permitidos

#### Build System
- **Backend**: NestJS
- **Frontend**: Next.js

#### Testing
- **Framework oficial**: Jest
- Aplicable a:
  - Lógica de negocio
  - Controladores
  - Servicios críticos

---

## 3. Restricciones de Implementación y Nomenclatura

### 3.1 APIs y Fuentes Dinámicas
- Está **prohibido** el uso de:
  - Listas estáticas de modelos
  - Listas estáticas de lenguajes
- Toda información de modelos o proveedores **debe resolverse dinámicamente** a través del `LlmModule`.

### 3.2 Convenciones de Código
- Los nombres de:
  - Variables
  - Funciones
  - Archivos
  - Directorios

**deben seguir estrictamente** las convenciones definidas en: @/specs/conventions.md

No se permiten excepciones ad-hoc.

### 3.3 Idioma de la Interfaz
- Se **prohíbe** el uso de términos en inglés en:
  - Textos de UI
  - Labels
  - Placeholders
  - Mensajes de error
- Toda la interfaz debe estar **estrictamente en Castellano**.

---

## 4. Referencias Cruzadas Obligatorias

Esta regla se apoya en las siguientes fuentes complementarias:

- **Identidad visual y estilos**  
  `@skills/digisite-branding`

- **Generación y estructura de código**  
  `@skills/code-gen`

Estas referencias deben activarse siempre que el contexto lo requiera.

---

## 5. Criterio de Cumplimiento

El incumplimiento de cualquiera de los puntos anteriores se considera:

- Violación de la regla central del proyecto
- Motivo suficiente para:
  - Rechazo de implementación
  - Reversión de cambios
  - Revisión técnica obligatoria

---