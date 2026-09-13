# Trazabilidad y fundamentación del diseño

**TP3, Parte 3.** Equipo NERO IT : producto A.N.A.N.A.

Acompaña a `docs/diseno/alternativas.md` (las tres alternativas recibidas), `docs/diseno/propuesta-final.md` (la propuesta elegida) y `docs/diseno/wireframe/` (el wireframe navegable).

Toda la evidencia citada en este documento está en `docs/evidencia/tp2/respuestas-encuesta-U1-U2-U3.csv`.

---

## 10.1 Anclaje

Tres decisiones concretas del wireframe, cada una con la pregunta de la encuesta que la sustenta, la respuesta textual de los usuarios y el análisis que conecta una cosa con la otra. Se agregan dos decisiones más que no se apoyan en el relevamiento y se identifican como tales: una es una suposición del equipo y la otra contradice un dato relevado.

### Decisión 1: la nota de privacidad aparece antes de la primera pregunta del check-in

**Pregunta.** "¿Qué le generaría dudas o le haría no probarla?"

**Respuesta.**

> **U3:** "Que solicite información privada sin un motivo claro"

**Análisis.** La objeción no es que se pregunte, sino que se pregunte sin explicar para qué. El obstáculo es la ausencia de motivo, no el pedido de información en sí. Por eso la explicación del uso del dato se ubica antes de la primera pregunta y dentro del propio formulario, en lugar de quedar en una pantalla de configuración o en un texto legal aparte. Si la nota apareciera después, el usuario respondería antes de saber qué pasa con su respuesta, que es exactamente la situación que le genera la duda.

### Decisión 2: la vista semanal ordena por prioridad con color y cercanía de fecha, no como lista plana

**Pregunta.** "¿Prefiere ver sus pendientes en una lista simple sin orden o agrupados por día con prioridad marcada?"

**Respuesta.**

> **U1:** "agrupados por día con prioridad marcada"
> **U2:** "agrupados por día con prioridad marcada"
> **U3:** "agrupados por día con prioridad marcada"

**Análisis.** Tres de tres, sin excepción: es el dato que confirmó el Supuesto 2 del TP1. La preferencia es unánime y no admite una lectura intermedia, así que la jerarquía de la pantalla se construye sobre el criterio de urgencia y no sobre el orden de carga ni el orden alfabético. El color no cumple una función decorativa: es el mecanismo por el cual el usuario identifica la próxima actividad importante sin tener que leer la lista completa.

### Decisión 3: el check-in tiene una salida explícita del mismo peso visual que el botón de envío

**Pregunta 1.** "Si una app le preguntara en menos de 2 minutos cómo se siente (respetando la privacidad de su información) ¿la usaría?"

**Respuesta 1.**

> **U1:** "No" · **U2:** "Sí" · **U3:** "Sí"

**Pregunta 2.** "¿Qué le generaría dudas o le haría no probarla?", referida al producto completo.

**Respuesta 2.**

> **U1:** "Nada, la probaría"

**Análisis.** U1 rechaza el check-in y, al mismo tiempo, no tiene ninguna objeción al resto del producto. Leídas juntas, las dos respuestas describen a un usuario que quiere la aplicación pero no esa función en particular. Si el check-in fuera obligatorio para avanzar, el diseño perdería a ese usuario entero por una función que él no pidió. La salida no es una concesión de cortesía: es lo que mantiene a U1 dentro del producto. Además, el Supuesto 4 quedó confirmado con dos de tres y no con tres de tres, de modo que el diseño está obligado a contemplar al tercero.

### Decisión 4: el flujo abre con el check-in y cierra con el resumen semanal. Esto es una suposición

**Pregunta.** Ninguna. La encuesta no preguntó en qué momento de la sesión los usuarios querrían registrar su estado, ni con qué pantalla esperarían empezar.

**Respuesta.** No hay dato relevado que sustente este orden.

**Análisis.** El orden se decidió por una razón interna del equipo: el check-in alimenta la alerta, así que tiene que ocurrir antes de que la alerta pueda mostrarse. Es un razonamiento coherente, pero es una deducción del equipo y no un hallazgo del relevamiento. Se deja identificada como suposición, y es uno de los puntos que conviene observar en la prueba del TP4: si los usuarios entran buscando primero su semana, el orden habrá que invertirlo.

### Decisión 5: el wireframe se diseña solo para pantalla de celular. Esto contradice un dato del relevamiento

**Pregunta.** "¿Desde qué dispositivo consulta habitualmente MIEL, mail o calendario?"

**Respuesta.**

> **U1:** "ambos" · **U2:** "ambos" · **U3:** "ambos"

**Análisis.** El dato dice lo contrario de lo que el diseño hace. El Supuesto 3, que asumía acceso principalmente desde el celular, quedó refutado: los tres alternan entre celular y computadora sin preferencia marcada. Aun así el equipo decidió construir el MVP solo para celular, y conviene precisar el motivo: no porque el relevamiento lo respalde, sino porque construir y probar dos interfaces excede lo que el equipo puede hacer en el tiempo disponible, y el celular es el caso más restrictivo en ancho, de modo que una estructura que funciona ahí puede expandirse después sin rehacer la navegación.

El costo se asume y se deja escrito: la prueba del MVP no va a decir nada sobre cómo se comporta el producto en computadora, que es la mitad del contexto de uso que el TP2 registró. Si en el TP4 aparece que los usuarios abandonan la herramienta cuando están frente a la computadora, la causa estará en este recorte y no en la hipótesis.

---

## 10.2 Descarte

Tres propuestas generadas por la IA que el equipo rechazó. Para cada una: qué propuso, por qué no y con qué se reemplazó.

### Descarte 1: pantalla de estadísticas con evolución histórica del ánimo

**Qué propuso.** Una pantalla con gráficos de evolución del estado de ánimo y del nivel de estrés a lo largo de las semanas, con promedios y tendencias, accesible desde el resumen.

**Por qué no.** A la pregunta *"¿Registra hoy en algún lado su estado de ánimo o nivel de estrés?"* los tres respondieron **"No"**: ninguno lleva ese registro hoy ni manifestó querer consultarlo. Y a la pregunta *"De las funcionalidades descriptas, ¿cuál le resolvería algo que hoy no tiene resuelto?"*:

> **U1:** "Me ayudaría a organizarme mejor"
> **U3:** "Me ayudaría a evitar la acumulación de tareas y a controlar mi estado emocional"

Los dos hablan de **organizarse** y de **evitar** la acumulación, no de analizar su propio historial. El valor que esperan es preventivo, no analítico. Además, la funcionalidad de estadísticas definida en el brief está dirigida al grupo de usuarios administrativo, de modo que llevarla a la interfaz del estudiante mezclaría dos grupos distintos.

**Con qué se reemplazó.** Con la pantalla de alerta preventiva. Usa exactamente los mismos datos que alimentarían los gráficos, pero los devuelve como un aviso accionable en el momento en que sirven, en lugar de como un informe que el usuario tendría que ir a buscar e interpretar por su cuenta.

### Descarte 2: rachas, puntos e insignias sobre el check-in

**Qué propuso.** Mostrar una racha de días consecutivos con check-in completado y otorgar insignias por constancia, con el objetivo de aumentar la adherencia.

**Por qué no.** La propuesta asume que el problema de adherencia es de motivación. El TP2 mostró que es de confianza:

> **U3:** "Que solicite información privada sin un motivo claro"
> **U1:** "No" (a si usaría el check-in), pero "Nada, la probaría" sobre el resto del producto

Una racha aumenta la presión justamente sobre el punto que ya genera desconfianza, y además introduce un incentivo para responder cualquier cosa con tal de no perderla. Eso contaminaría el dato que alimenta la alerta, que es el núcleo del producto.

**Con qué se reemplazó.** Con dos elementos que atacan la confianza en lugar de la motivación: la nota de privacidad al inicio del check-in, y el botón "Ahora no" con el mismo peso visual que el de envío. La adherencia se busca dando control, no premiando la constancia.

### Descarte 3: la alerta preventiva resuelta como notificación breve

**Qué propuso.** Resolver la alerta como una notificación push corta o un cartel emergente con el texto del aviso y un botón para cerrarlo.

**Por qué no.** Repite el patrón que U3 rechazó, que es la información que llega sin motivo explicado. Una notificación breve comunica una conclusión sobre el estado emocional del usuario sin decirle de dónde salió. Además contradice la definición del producto en el brief, donde A.N.A.N.A. es preventiva y explícitamente no realiza diagnósticos: un aviso sin contexto se lee como un diagnóstico.

**Con qué se reemplazó.** Con una pantalla de acompañamiento que primero explica el origen del aviso en términos verificables por el usuario ("tenés 4 entregas en los próximos 7 días y marcaste estrés alto en tus últimos 3 check-ins") y no propone ninguna acción: el estudiante decide qué hacer con esa información. La pantalla da el motivo, no un diagnóstico ni un plan, y el usuario puede reconstruir por qué apareció y desestimarlo si no coincide con su situación.

---

## 10.3 El elemento crítico

### ¿Cuál es el elemento que sostiene la hipótesis?

**El elemento que sostiene la hipótesis es la detección preventiva de sobrecarga**, es decir el cruce entre entregas próximas y check-ins y la alerta que resulta de él.

La hipótesis se verifica con dos observaciones: que los usuarios reemplacen su método actual y que al menos 2 de cada 3 sostengan el check-in. Sin el cruce, el check-in queda sin propósito visible y nadie lo sostiene una semana, con lo cual la segunda observación daría negativo por una razón de diseño y no porque la hipótesis sea falsa. Y sin la alerta, lo que queda es un organizador más compitiendo con WhatsApp y la agenda del celular, de modo que el Supuesto 5, el supuesto crítico, quedaría sin poder confirmarse ni refutarse.

### ¿Hay algo incluido que podrían sacar sin perder esa capacidad?

| Elemento incluido | ¿El experimento pierde validez sin esto? | Por qué |
|---|---|---|
| Organización de materias, entregas y eventos | Sí | Sin datos cargados no hay nada que cruzar ni nada que reemplazar. |
| Check-in de bienestar | Sí | Es una de las dos observaciones con las que se verifica la hipótesis. |
| Detección preventiva de sobrecarga | Sí | Es el elemento crítico. |
| Dashboard y checklist semanal | No | El cruce necesita los datos, no la vista. |
| Uso desde el celular | No | Es una restricción del equipo, no un requisito del experimento. |

El dashboard y checklist semanal no es necesario para el experimento: la alerta se calcula sobre los datos cargados, no sobre cómo se muestran, y las dos observaciones se podrían hacer con un listado simple ordenado por fecha. Quedó adentro por dos razones, y ninguna es experimental. La primera es que el Supuesto 2 ya está confirmado con tres respuestas de tres, así que darles deliberadamente el formato que descartaron sería empeorar la experiencia a propósito. La segunda es que, según el punto 1 de este mismo trabajo, es justamente la vista priorizada lo que distingue a A.N.A.N.A. de un calendario convencional: sacarla dejaría al MVP probando un producto distinto del que definimos.

El uso desde el celular tampoco resiste el filtro: el experimento sería igual de válido en cualquier dispositivo. Quedó adentro porque el equipo no puede construir y probar dos interfaces en el tiempo disponible, tal como se explica en el 10.1. Es una restricción de capacidad, no una condición del experimento.

**Lo que el ejercicio deja a la vista** es que el MVP está ajustado: de cinco elementos, tres son imprescindibles y los dos que sobran están por razones que el equipo puede nombrar, una de coherencia con el producto y otra de capacidad.
