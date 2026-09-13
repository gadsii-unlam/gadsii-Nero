# Decisiones de diseño: jerarquía, navegación y flujo (TP3)

Equipo NERO IT : producto A.N.A.N.A.
Describe la estructura del wireframe de baja fidelidad que se encuentra en `docs/diseno/wireframe/`.

El wireframe corresponde a la Alternativa B, que privilegia la satisfacción y la confianza como atributo de usabilidad principal. La justificación de esa elección está en `docs/diseno/alternativas.md` y el respaldo en evidencia del TP2 está en `docs/diseno/fundamentacion.md`.

---

## Jerarquía de información

En la pantalla de check-in (1), que es la de apertura, la nota de privacidad tiene la jerarquía más alta: aparece primero, antes que la pregunta en sí, porque el TP2 mostró que la confianza es la barrera principal (Usuario 3 dudaba de "que solicite información privada sin motivo claro"). La escala de ánimo es el segundo nivel y el nivel de estrés queda tercero. La opción de saltear el check-in ("Ahora no") está presente pero con peso visual secundario: se puede omitir, pero no es lo primero que se ofrece.

En la pantalla de alerta preventiva (2) hay un solo elemento con jerarquía: el mensaje con el motivo concreto que disparó el aviso, en un bloque destacado y no como un ícono suelto ni una notificación seca. No hay opciones ni acciones sugeridas debajo, porque la alerta advierte y no reorganiza: se prioriza que el usuario entienda por qué apareció y decida él qué hacer.

En la pantalla de agregar entrega (3), los campos siguen el orden en que el estudiante piensa la información (materia, título, fecha, tipo) y la confirmación visual de guardado tiene jerarquía propia: aparece como bloque explícito antes de volver al resumen, no como un cambio silencioso.

En la pantalla de resumen semanal (4), que cierra la sesión, el elemento de mayor jerarquía visual es la vista semanal ordenada por prioridad (color más cercanía de fecha), no una lista plana, porque responde directamente al Supuesto 2 confirmado en el TP2. El mensaje de bienvenida queda arriba pero con menor peso, como texto breve y no como acción. Los botones de acción quedan al final, como segundo nivel: se llega a ellos después de ver el panorama de la semana, no antes.

## Navegación

La navegación del recorrido principal es secuencial y guiada: el usuario avanza paso a paso desde el check-in hasta el resumen, sin tener que decidir por dónde empezar. Cada paso ofrece una salida explícita ("Ahora no", "No por ahora") que no interrumpe el recorrido sino que saltea ese paso y continúa al siguiente, de modo que ninguna pantalla es un callejón sin salida ni una obligación.

La pantalla de alerta preventiva (2) es el único paso condicional: no se accede por decisión del usuario, sino que aparece cuando el cruce de entregas próximas y check-ins indica sobrecarga. Si no corresponde, el recorrido pasa directo del check-in a la carga de entregas.

La pantalla de resumen semanal (4) cumple una doble función: cierra el recorrido principal y, en visitas posteriores dentro del mismo día, funciona como pantalla ancla desde la cual se puede volver a agregar una entrega o rehacer el check-in sin repetir toda la secuencia. Es decir, el primer ingreso del día es lineal y el resto de las consultas parten del resumen.

No hay menús anidados ni jerarquías de más de un nivel: todas las pantallas están a un paso de la anterior o del resumen.

## Flujo

El recorrido principal reproduce el flujo definido en la Parte 1 del TP3. El estudiante abre A.N.A.N.A. un lunes a la mañana y recibe el pedido de check-in breve de ánimo y estrés (pantalla 1). Si el cruce de entregas próximas y check-ins indica sobrecarga, ve la alerta preventiva con el motivo concreto que la disparó (pantalla 2). Luego carga una entrega o evento nuevo si le falta alguno (pantalla 3). Finalmente llega a su vista semanal con materias y entregas ordenadas por prioridad, que cierra la sesión como dashboard con la información clave para organizar la semana (pantalla 4).

Es un solo flujo principal, sin bifurcaciones que compitan en importancia, tal como pide la consigna. Los pasos 2 y 3 son condicionales u opcionales, pero no constituyen flujos alternativos: son ramas del mismo recorrido que desembocan siempre en la misma pantalla de cierre.

---

## Nota sobre fidelidad

El wireframe es deliberadamente de baja fidelidad: escala de grises, bloques punteados, líneas de texto simuladas y ausencia de identidad visual. El objetivo es que la discusión durante la prueba se concentre en la estructura y el recorrido, y no en colores, tipografías o estilo. Las únicas excepciones cromáticas son funcionales: los indicadores de prioridad en la vista semanal y el bloque de alerta, donde el color transmite información y no decoración.

Las anotaciones amarillas sobre el wireframe explican la decisión de diseño de cada pantalla y su vínculo con la evidencia del TP2. No forman parte de la interfaz.
