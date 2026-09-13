# Alternativas de diseño evaluadas (TP3, Parte 2)

Equipo NERO IT : producto A.N.A.N.A.

Se generaron tres alternativas de diseño para el mismo flujo principal definido en la Parte 1. Cada una privilegia un atributo de usabilidad distinto de los priorizados por el equipo, de modo que la comparación sea real y no una variación estética.

El flujo es siempre el mismo: check-in de bienestar, alerta preventiva condicional, carga de entrega o evento, y resumen semanal de cierre. Lo que cambia entre alternativas es cómo se estructura la interacción para llegar a ese resultado.

---

## Alternativa A: privilegia la eficiencia

**Idea central:** minimizar la cantidad de toques y de pantallas. Todo ocurre sobre el resumen semanal.

**Cómo se resuelve:** el check-in aparece como una fila compacta dentro del propio resumen, con cinco caritas en línea que se responden con un solo toque y sin cambiar de pantalla. La carga de una entrega se hace en una ventana modal superpuesta que no abandona el contexto. La alerta preventiva aparece como una franja en la parte superior del resumen.

**Qué gana:** un usuario que ya conoce la aplicación resuelve toda su sesión en una sola pantalla y en pocos segundos. Es la alternativa con menor cantidad de pasos.

**Qué pierde:** no hay lugar para explicar por qué se pide el dato de bienestar antes de pedirlo. La nota de privacidad quedaría como un ícono de información o un texto secundario. La alerta preventiva, reducida a una franja, comunica un estado sin explicar su origen.

---

## Alternativa B: privilegia la satisfacción y la confianza (alternativa elegida)

**Idea central:** que cada paso sensible venga acompañado de su explicación y de una salida clara, aunque eso cueste una pantalla más.

**Cómo se resuelve:** el check-in ocupa su propia pantalla y abre con la nota de privacidad antes de cualquier pregunta. La alerta preventiva es una pantalla de acompañamiento que explica el motivo del aviso y ofrece opciones, en lugar de comunicar un dato aislado. La carga de entregas ocurre en pantalla propia con confirmación visual explícita. El recorrido es secuencial y cada paso tiene una salida que permite saltearlo sin insistencia.

**Qué gana:** aborda directamente la barrera de confianza detectada en el TP2 y sostiene el carácter preventivo y de acompañamiento del producto.

**Qué pierde:** requiere más pantallas y más toques que la Alternativa A. Un usuario frecuente puede sentir el recorrido algo largo una vez que ya confía en la herramienta.

---

## Alternativa C: privilegia la facilidad de aprendizaje y el recuerdo en el tiempo

**Idea central:** que la estructura sea evidente desde el primer uso mediante navegación permanente por secciones.

**Cómo se resuelve:** una barra inferior fija con tres secciones (Semana, Bienestar, Agregar) siempre visible. El usuario no sigue un recorrido guiado sino que elige en qué sección entrar. Un asistente de primer uso recorre las secciones al inicio. La alerta aparece como distintivo numérico sobre la sección de Bienestar.

**Qué gana:** el modelo mental es inmediato y familiar, y se recuerda bien después de semanas sin usar la aplicación.

**Qué pierde:** al ofrecer tres entradas de igual jerarquía, el producto se presenta como tres funciones sueltas en lugar de una experiencia integrada. Esto debilita justamente lo que distingue a A.N.A.N.A., que es el cruce entre carga académica y bienestar. Además, si el usuario nunca entra a la sección de Bienestar, la alerta preventiva no llega a cumplir su función.

---

## Elección y justificación

| Criterio | Alternativa A (eficiencia) | Alternativa B (satisfacción y confianza) | Alternativa C (aprendizaje y recuerdo) |
|---|---|---|---|
| Atributo de usabilidad priorizado | Eficiencia | Satisfacción y confianza | Facilidad de aprendizaje y recuerdo |
| Responde a la barrera de confianza del TP2 | No, la explicación queda relegada | Sí, la nota de privacidad antecede a la pregunta | Parcialmente, depende de que el usuario entre a la sección |
| Sostiene el cruce carga académica y bienestar | Sí, pero de forma implícita | Sí, es el eje del recorrido | No, presenta las funciones como secciones separadas |
| Adecuación al carácter preventivo del producto | Baja, la alerta queda reducida a un aviso | Alta, la alerta se presenta con contexto y opciones | Media, la alerta depende de un distintivo numérico |
| Costo en cantidad de pantallas y pasos | El más bajo | Intermedio | Intermedio |
| Riesgo principal | Perder la confianza del usuario en el check-in | Recorrido percibido como largo por usuarios frecuentes | Que el producto se perciba como tres herramientas sueltas |

**Alternativa elegida: B.**

La decisión se tomó porque el relevamiento del TP2 mostró que el obstáculo principal para el uso del producto no es la cantidad de pasos sino la confianza en el tratamiento del dato de bienestar. Optimizar la eficiencia (Alternativa A) mejora un aspecto que ningún usuario señaló como problema, a costa de agravar el que sí señalaron. La Alternativa C, por su parte, resuelve bien el aprendizaje inicial pero desarma el cruce entre organización académica y bienestar, que es exactamente el elemento crítico que sostiene la hipótesis de valor.

El costo asumido, un recorrido con más pasos que el mínimo posible, se considera aceptable en esta etapa porque lo que el MVP pone a prueba es si el usuario confía lo suficiente como para completar el check-in y encuentra valor en la alerta resultante. Si esa hipótesis se valida, la eficiencia puede optimizarse en iteraciones posteriores sin rehacer la estructura.
