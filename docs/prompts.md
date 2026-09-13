# Registro de trabajo con IA

Este archivo registra las interacciones del equipo con herramientas de inteligencia artificial durante la cursada, según lo exigido por la cátedra.

**Criterio del equipo.** Ningún hallazgo del relevamiento se atribuye a la IA: todo hallazgo es rastreable a la evidencia de campo versionada en `docs/evidencia/`. En el TP3, las decisiones de la Parte 1 (alcance del MVP, qué se construye y qué se simula, atributos de usabilidad priorizados) fueron tomadas por el equipo antes de delegar la Parte 2. La IA se usó para generar alternativas de diseño, producir el wireframe y ordenar la documentación.

**Convención de commits.** Los commits que incorporan material generado con IA se marcan con `(AI-assisted)` al final del mensaje. Ejemplo:

```
docs(diseno): agregar wireframe navegable del MVP (AI-assisted)
```

---

## TP2 : Análisis de usuarios e hipótesis de valor

Herramienta: Claude (Anthropic), vía Claude Cowork.

| # | Fecha | Prompt (resumen) |
|---|---|---|
| 1 | 01/09/2026 | Revisar la consigna del TP2 y armar un checklist de cumplimiento contra el enunciado de la cátedra. |
| 2 | 01/09/2026 | Redactar una guía de preguntas para el relevamiento, revisando que no haya preguntas capciosas o que induzcan la respuesta. |
| 3 | 01/09/2026 | Convertir la guía a formato de encuesta autoadministrada y generar la planilla de respuestas para U1, U2 y U3. |
| 4 | 01/09/2026 | Reescribir tres preguntas que mencionaban el producto por su nombre, e incorporar un bloque de contexto antes de las preguntas de intención de uso, dado que la encuesta es autoadministrada. |
| 5 | 01/09/2026 | Ordenar las respuestas ya relevadas por el equipo en las tablas de perfil, necesidades, problemas y contexto de uso, y en la tabla de confrontación de supuestos. |
| 6 | 01/09/2026 | Revisar la redacción de la hipótesis de valor sobre el formato pedido por la cátedra. |
| 7 | 13/09/2026 | Redactar el brief de producto versión 2 a partir del informe entregado, y preparar los archivos de evidencia anonimizados para versionar en `docs/evidencia/tp2/`. |

---

## TP3 : Scope del MVP y diseño

Herramienta: Claude (Anthropic), vía Claude Cowork. Todos los intercambios de esta sección ocurrieron el **13/09/2026**, en el orden en que se listan.

### Parte 1 : discusión previa a la delegación

Estos intercambios no delegan decisiones: la IA actuó como contraparte para discutir, y las definiciones las tomó el equipo.

| # | Prompt |
|---|---|
| 1 | "Tengo que hacer el TP3. ¿Hacemos como lo del otro día?" (adjuntando la consigna del TP3 y el material de la Clase 3) |
| 2 | Revisar la devolución del TP1 y explicar la observación sobre la cantidad de funcionalidades core. |
| 3 | "Hablo de las funcionalidades, centrate en eso": analizar el recorte de seis funcionalidades core a cuatro. |
| 4 | "Revisemos esto: qué se construye y qué se simula": discutir la tabla de construcción y simulación del MVP. |
| 5 | "Punto 4, qué dice sobre atributos de usabilidad": explicar los atributos de usabilidad de la Clase 3 y discutir cuáles priorizar. |
| 6 | "El flujo que definí yo fue este: [cinco pasos del recorrido del estudiante]". Corrección del equipo sobre el flujo principal, que la IA había supuesto distinto. |

### Parte 2 : generación de alternativas y wireframe

| # | Prompt |
|---|---|
| 7 | "Vamos con la parte 2": generar tres alternativas de diseño para el mismo flujo, cada una privilegiando un atributo de usabilidad distinto, más la tabla comparativa para fundamentar la elección. |
| 8 | Construir el wireframe navegable de baja fidelidad, con un mínimo de tres pantallas, navegación entre ellas y anotaciones de las decisiones de diseño. |
| 9 | "Fotos diferentes con explicaciones, PNG, no HTML": generar capturas de cada pantalla del wireframe para el cuerpo del informe, manteniendo el HTML navegable como entregable. |
| 10 | "Jerarquía de información, navegación y flujo": redactar la descripción estructural del wireframe. |
| 11 | "¿Qué es hub and spoke?": consulta conceptual sobre el patrón de navegación mencionado en la respuesta anterior. |
| 12 | Corregir el wireframe para que el orden de las pantallas siga el flujo principal definido por el equipo en el prompt 6, en lugar del que había supuesto la IA. |

### Parte 3 : ordenamiento de la documentación

| # | Prompt |
|---|---|
| 13 | Crear la carpeta de trabajo del TP3 y generar los borradores de los archivos que pide la consigna. |
| 14 | Leer el informe del TP2 y el repositorio, y generar los borradores de lo que hay que versionar en git. |
| 15 | Redactar la Parte 3: anclaje de decisiones en citas textuales del TP2, descarte de propuestas con el dato que las contradice y su reemplazo, y definición del elemento crítico del MVP. |

### Correcciones del equipo sobre lo producido por la IA

Se dejan registradas porque muestran dónde la Parte 1 gobernó a la Parte 2:

- **Prompt 6.** La IA había organizado el wireframe con la vista semanal como pantalla de entrada. El equipo corrigió el orden según el flujo principal que había definido: el recorrido abre con el check-in y cierra con el resumen.
- **Prompt 14.** La IA justificó el alcance móvil afirmando que el celular era "el dispositivo principal del segmento". El equipo corrigió ese fundamento contra el dato del TP2 que refutó el Supuesto 3, donde los tres respondieron "ambos": el MVP se limita al celular por una restricción de capacidad del equipo y no porque el relevamiento lo respalde. La decisión y su costo quedan declarados en `docs/diseno/fundamentacion.md`, decisión 5.
- Las propuestas de diseño rechazadas y su fundamento están documentadas en `docs/diseno/fundamentacion.md`, sección 10.2.
