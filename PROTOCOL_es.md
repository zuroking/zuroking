# PROTOCOL.md: Ecosistema de Desarrollo Basado en Habilidades (Skill-Driven Development)

**Languages:** [English](PROTOCOL.md) · [Русский](PROTOCOL_ru.md) · [العربية](PROTOCOL_ar.md) · [中文](PROTOCOL_zh.md) · [Deutsch](PROTOCOL_de.md) · **Español** · [Français](PROTOCOL_fr.md) · [日本語](PROTOCOL_ja.md) · [한국어](PROTOCOL_ko.md) · [Português](PROTOCOL_pt.md)

## 1. Concepto y Filosofía

Este documento describe la metodología de desarrollo dentro del portafolio, adaptada para un ecosistema de agentes híbrido. El protocolo cubre todo el ciclo de vida del producto — desde el borrador inicial de arquitectura hasta la generación final de artefactos de presentación.

Principio fundamental: **Las decisiones arquitectónicas deben ser explícitas, reproducibles y defendibles.** Hemos pasado de simplemente escribir código a un **Desarrollo Basado en Habilidades (Skill-Driven Development)**, donde las operaciones rutinarias, el diseño, las pruebas y los análisis se delegan a habilidades especializadas de agentes específicos.

---

## 2. Roles y Distribución de Habilidades

Tres entidades principales y el entorno de agentes unificado participan en el proceso. Sus roles están estrictamente separados y no se superponen.

### 2.1. Developer (Humano)
El propietario del producto. Tiene la última palabra en cada punto de decisión arquitectónica, aprueba el alcance, establece la dirección del desarrollo y acepta los entregables de los agentes.

### 2.2. OpenCode (Implementador Autónomo)
El agente ejecutor, que opera en la terminal con una ventana de contexto de hasta 1M de tokens. Responsable de escribir código, construir interfaces y generar documentos y artefactos multimedia.
Posee el siguiente arsenal de habilidades:
*   **Ingeniería y Código:** `code-review-skill`, `webapp-testing`, `mcp-builder`, `skill-creator`, `claude-api`.
*   **Diseño y Frontend:** `frontend-design`, `web-artifacts-builder`, `theme-factory`, `canvas-design`, `algorithmic-art`, `brand-guidelines`.
*   **Documentación y Oficina:** `build-project-docs`, `doc-coauthoring`, `docx`, `pdf`, `pptx`, `xlsx`.
*   **Comunicación y Capacitación:** `academy-guide`, `internal-comms`, `slack-gif-creator`, `discernment-nudge`.

### 2.3. Claude Desktop (Arquitecto y Analista)
Actúa como centro de datos y revisor arquitectónico. No escribe código de producción directamente, sino que verifica la lógica, analiza los datos de la base de datos y formula tareas para OpenCode.
Arsenal de habilidades:
*   **Gestión de Contexto:** `morning`, `Import-memory`, `skill-creator`, `doc-coauthoring`.
*   **Análisis y Validación:** `analyze`, `data-context-extractor`, `explore-data`, `validate-data`, `statistical-analysis`.
*   **Base de Datos y Visualización de Datos:** `sql-queries`, `write-query`, `build-dashboard`, `create-viz`, `data-visualization`.

### 2.4. Antigravity (Entorno de Agentes Unificado)
Un entorno completamente autónomo que integra el conjunto completo de 33 habilidades.
*   **Regla clave:** A partir de ahora, toda la documentación del proyecto debe crearse y mantenerse exclusivamente a través de Antigravity, utilizando los modelos Gemini y Claude (como las mejores herramientas de documentación con acceso sin restricciones a las habilidades).

---

## 3. Etapas del Protocolo (Ciclo de Vida del Proyecto)

### Etapa 1: Inicialización y ARCHITECTURE.md
La arquitectura se formula antes de escribir una sola línea de código.
1.  **Claude Desktop** activa las habilidades `morning` and `Import-memory` para cargar el contexto y el trabajo anterior. Luego aplica `analyze` para descomponer los requisitos.
2.  **OpenCode** utiliza `build-project-docs` para crear un borrador de `ARCHITECTURE.md`.
3.  El documento se consolida: estructuras de datos, formatos de almacenamiento, pila tecnológica y desglose de módulos.

### Etapa 2: Grill-me (Prueba de Estrés de la Arquitectura)
La arquitectura no se acepta por fe. Debe ser atacada y cuestionada.
1.  **Claude Desktop** aplica `data-context-extractor` para identificar "puntos ciegos" en los datos y `doc-coauthoring` para generar preguntas incómodas.
2.  **OpenCode** puede utilizar `discernment-nudge` para una autoevaluación crítica de las soluciones técnicas propuestas.
3.  Cada punto de decisión polémico se cierra con una tríada: **solución elegida -> razón para rechazar la alternativa -> exclusiones del alcance**.

### Etapa 3: Desviaciones Deliberadas (Deliberate Deviations)
Una sección en `ARCHITECTURE.md` donde registramos todas las características y capacidades que **elegimos conscientemente no construir**. El límite de las capacidades de un proyecto es parte integral de su arquitectura. Si una decisión cambia durante el desarrollo, la decisión anterior se traslada aquí junto con la razón.

### Etapa 4: Implementación Módulo por Módulo
El desarrollo avanza de abajo hacia arriba a lo largo del grafo de dependencias.
1.  **OpenCode** implementa el núcleo del proyecto. Para integraciones y protocolos, se utilizan `mcp-builder` y `claude-api`.
2.  Al trabajar en el aspecto visual, **OpenCode** activa la cadena: `brand-guidelines` -> `theme-factory` -> `frontend-design` -> `web-artifacts-builder`.
3.  Para la generación de gráficos procedimentales o lienzos complejos, se aplican `algorithmic-art` y `canvas-design`.

### Etapa 5: Revisión de Código y Pruebas
La verificación siempre se separa de la escritura del código.
1.  **OpenCode** realiza una pasada independiente utilizando `code-review-skill`, identificando errores y concesiones.
2.  Las pruebas de interfaz de usuario e integración se realizan a través de la habilidad `webapp-testing`. La salida de las pruebas (stdout/stderr) se guarda sin modificaciones.
3.  **Claude Desktop** interviene para verificar el manejo de datos: utiliza `sql-queries` y `write-query` para comprobar la integridad de la base de datos, junto con `validate-data` y `statistical-analysis` para verificar la lógica de negocio.

### Etapa 6: Generación de Artefactos y Análisis
El proyecto debe ser presentado al usuario o a las partes interesadas.
1.  **Claude Desktop**, utilizando `build-dashboard`, `create-viz` y `data-visualization`, genera informes basados en los resultados o métricas de la aplicación.
2.  **OpenCode** empaqueta estos datos en artefactos comerciales listos para usar:
    *   Informes y especificaciones: habilidades `pdf`, `docx`, `xlsx`.
    *   Presentaciones de arquitectura: habilidad `pptx`.
    *   Materiales de capacitación e internos: `academy-guide`, `internal-comms`.
    *   Contenido dinámico para anuncios: `slack-gif-creator`.

### Etapa 7: Lista de Verificación Final
Antes del lanzamiento, se verifica lo siguiente:
*   Sincronización del código final con `ARCHITECTURE.md`.
*   Presencia de registros de pruebas reales.
*   Ausencia de archivos temporales, cachés y claves secretas.

---

## 4. Política de Selección de Modelos (Model Selection Policy)

OpenCode se ejecuta en modelos gratuitos, cuya elección está dictada por la tarea:

| Modelo | Rol | Propósito | Estado de Privacidad |
| :--- | :--- | :--- | :--- |
| **Muse Spark 1.2 Free** | Agente Autónomo (Core) | Ejecución de la matriz principal de habilidades, contexto de 1M de tokens, lógica de múltiples pasos en la terminal. | Nivel gratuito permanente |
| **Nemotron 3 Ultra Free** | Analista Profundo | Matemáticas pesadas, algoritmos complejos, refactorización del sistema a gran escala. | **Prueba de NVIDIA** — los datos se registran para mejorar el producto. |
| **Nemotron 3.5 Lightning Free** | Ejecutor en Segundo Plano | Validación rápida, llamadas a funciones utilitarias, procesamiento masivo. | **Prueba de NVIDIA** — igual que Ultra. |
| **MiMo V2.5 Free** | Asistente de UI/UX | Depuración de capturas de pantalla, `frontend-design` sobre la marcha. | Período gratuito temporal. |

Para **Antigravity**, se utiliza **Gemini 3.5 Flash (Medium)** como motor principal para garantizar el consumo mínimo de límites/cuotas y permitir el trabajo continuo en tareas y documentación.

**Restricción de Seguridad:** Está **estrictamente prohibido** pasar claves privadas, tokens, bases de datos reales y repositorios privados a puntos finales de prueba (Nemotron, MiMo). Solo se utiliza un entorno local o de confianza para datos confidenciales.

---

## 5. Principios Fundamentales del Ecosistema

1. **Una decisión explícita es mejor que un valor predeterminado conveniente.** Si un agente llega a una encrucijada, no adivina; formula opciones y espera la aprobación (o registra una concesión).
2. **Las habilidades se utilizan para el propósito previsto.** No hay necesidad de generar tablas de Markdown si se requiere un informe de Excel (use `xlsx`). No hay necesidad de describir un panel en texto (use `build-dashboard` + `create-viz`).
3. **Un error detectado en la revisión significa un sistema que funciona.** Un hallazgo durante la etapa de revisión a través de `code-review-skill` es prueba de que el filtro de dos etapas funciona.
4. **Los límites del proyecto son inviolables.** Una herramienta a medio terminar que lo hace todo es peor que una herramienta altamente especializada con una sección de Desviaciones Deliberadas (Deliberate Deviations) claramente documentada.
