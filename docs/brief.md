# Brief de Producto

<!-- Versión 2 — TP2. Cada versión siguiente abre con un párrafo de qué cambió y por qué. -->

## Qué cambió respecto de la versión 1

Esta segunda versión incorpora el relevamiento realizado con tres usuarios reales del grupo primario (U1, U2 y U3) durante la semana del 25/08/2026, mediante encuesta autoadministrada. La evidencia está versionada en `docs/evidencia/tp2/`.

Los cambios principales son tres. Primero, el perfil hipotético de usuario de la versión 1 se reemplaza por el perfil real construido con los datos relevados. Segundo, se incorporan las necesidades, los problemas y el contexto de uso tal como los describieron los usuarios, junto con la hipótesis de valor que surge de ellos. Tercero, y más importante para el diseño, **el Supuesto 3 quedó refutado**: el equipo asumía un acceso principalmente desde el celular y los tres usuarios respondieron que consultan desde ambos dispositivos sin preferencia marcada, de modo que el producto no puede diseñarse como una aplicación exclusivamente móvil.

Lo que no cambió es el segmento, el problema que el producto resuelve y la elección del usuario primario: el relevamiento los sostuvo. El supuesto crítico, el Supuesto 5, quedó confirmado.

---

## Segmento elegido

El segmento elegido está compuesto por estudiantes regulares de carreras de pregrado y grado de la UNLaM que, debido al trabajo, responsabilidades familiares, o cualquier otro motivo personal, experimentan ansiedad, estrés, posible sobrecarga emocional y dificultades recurrentes de organización y rendimiento académico.

La evaluación externa de la UNLaM registra un universo total de 43.865 estudiantes. Como todavía no existe una medición institucional que cruce cursada, trabajo, responsabilidades y situación emocional, estimamos que el segmento podría representar entre el 20 % y el 35 % de ese universo, es decir, aproximadamente entre 9.000 y 15.000 estudiantes. Sigue siendo una estimación de trabajo: el relevamiento del TP2 no permite corregirla, porque con tres usuarios los resultados indican dirección y no proporción.

Elegimos este segmento porque enfrenta un problema concreto y frecuente: la coordinación de materias, fechas de entrega, evaluaciones, trabajo y responsabilidades personales puede generar olvidos, dificultad para establecer prioridades y una experiencia negativa en los estudiantes. El relevamiento confirmó ese diagnóstico: los tres usuarios se olvidaron o se enteraron tarde de una entrega o parcial en el último cuatrimestre, y los tres sienten con frecuencia que tienen más responsabilidades de las que pueden manejar.

## Producto

### Nombre

El producto se denomina **A.N.A.N.A.: Ayuda y Notificaciones Académicas con Navegación Asistida**.

### Problema que resuelve

A.N.A.N.A. resuelve la dificultad de los estudiantes para centralizar sus obligaciones académicas, determinar prioridades y advertir tempranamente situaciones personales de sobrecarga.

La aplicación les ofrece un espacio privado donde pueden registrar materias, entregas, eventos y su estado general, obteniendo una vista integrada de su semana.

A.N.A.N.A. es una herramienta preventiva. No realiza diagnósticos clínicos, no interpreta enfermedades y no reemplaza la asistencia de profesionales de la salud.

### A quién le resuelve el problema

El producto está dirigido principalmente a los estudiantes del segmento seleccionado. El relevamiento sostuvo esta definición: los tres usuarios pertenecen al segmento, presentan el mismo patrón de sobrecarga frecuente y ausencia de método unificado, y los tres manifestaron que reemplazarían su forma actual de organizarse por A.N.A.N.A.

## Funcionalidades core

1. **Organización de materias, entregas y eventos.** El estudiante puede registrar las materias que cursa, fechas de entrega, evaluaciones y otros compromisos académicos.
2. **Dashboard y checklist semanal.** La plataforma genera una vista de las actividades pendientes, las prioridades y el progreso de la semana a partir de los datos reales cargados por el estudiante. El relevamiento confirmó que los tres usuarios prefieren esta vista agrupada por día con prioridad antes que una lista plana.
3. **Check-in de bienestar.** El estudiante puede registrar periódicamente su estado de ánimo, nivel de energía, estrés y carga percibida mediante una interacción breve y privada.
4. **Detección preventiva de sobrecarga.** La aplicación relaciona la cercanía de las obligaciones con los check-ins y presenta advertencias preventivas cuando identifica una acumulación de tareas o niveles elevados de carga.

5. **Relevamiento de estadísticas.** Usuarios administradores de la universidad pueden tener acceso a estadísticas anónimas de niveles promedio de sobrecarga, principales motivos y observaciones desglosados por carrera.
6. **Acceso a canales de ayuda.** El usuario puede acceder a diversos canales de comunicación proporcionados por la universidad para pedir asistencia.

## Integraciones previstas

* **Supabase Auth:** permite registrar usuarios, iniciar sesión y administrar identidades sin almacenar contraseñas directamente en la aplicación.
* **Supabase PostgreSQL:** proporciona persistencia para perfiles, materias, entregas, eventos y check-ins.
* **Formato iCalendar:** previsto para una etapa posterior, permitiría importar o exportar fechas con calendarios personales, siempre mediante autorización explícita del usuario.
* **Canales institucionales de apoyo:** integración futura, sujeta a validar responsables, datos y protocolos con la UNLaM.

El producto requiere un front-end y un back-end de desarrollo propio. La interfaz, la lógica del dashboard, el checklist, el cálculo preventivo de sobrecarga, las validaciones y las operaciones sobre los datos son desarrollados por el equipo utilizando Next.js, React, TypeScript y Server Actions.

## Grupos de usuarios

### Estudiantes del segmento seleccionado

Son estudiantes regulares que combinan la cursada con trabajo o responsabilidades familiares y necesitan organizar obligaciones provenientes de distintos espacios. Se encuentran directamente afectados por el problema y utilizarían A.N.A.N.A. para planificar, establecer prioridades y registrar su nivel de carga.

Este es el **grupo de usuarios primario**. Tras el relevamiento del TP2 la elección **deja de ser hipotética y queda sostenida en evidencia**: los tres usuarios analizados pertenecen al segmento, muestran el problema y expresaron intención de reemplazar su método actual.

### Equipos universitarios de bienestar y acompañamiento

Profesionales y áreas institucionales vinculadas con bienestar estudiantil, orientación y acompañamiento de trayectorias. Podrían utilizar indicadores agregados y anónimos para reconocer tendencias generales. No accederían a check-ins ni a datos personales de estudiantes individuales.

### Autoridades y responsables institucionales

Personas que podrían evaluar la implementación de la plataforma en la Universidad. Su motivación sería contar con una herramienta preventiva que contribuya a la permanencia y al bienestar estudiantil.

---

## Perfil del usuario real

Reemplaza al perfil hipotético de la versión 1. Construido con los datos de U1, U2 y U3.

| | U1 | U2 | U3 |
|---|---|---|---|
| **Perfil** | 4to año de Ing. Informática, cursa 6 materias, trabaja unas 6 horas por día, sin responsabilidades familiares regulares. | 4to año de Ing. Informática, cursa 6 materias, trabaja unas 9 horas por día, la mayor carga laboral de los tres, sin responsabilidades familiares regulares. | 4to año de Ing. Informática, cursa 6 materias, no trabaja actualmente, sin responsabilidades familiares regulares. |
| **Necesidades reales** | Hoy organiza sus entregas por WhatsApp. Necesita un lugar único donde no tener que buscar la información dispersa en conversaciones. Prefiere vista agrupada por día con prioridad antes que lista plana. | Hoy no usa ninguna herramienta. Necesita un sistema de organización desde cero: parte del punto más bajo de los tres. Igual que los otros, prefiere vista agrupada por prioridad. | Hoy organiza con la agenda del celular. Necesita algo que resuelva la coordinación con otras personas, no solo el registro individual de tareas. También prefiere vista agrupada por día con prioridad. |
| **Problemas y frustraciones** | "Es incómodo buscarlo": la información de entregas queda dispersa en WhatsApp. Se enteró tarde u olvidó una entrega o parcial el último cuatrimestre. No usaría el check-in de bienestar tal como está planteado. | "No tengo organización": ausencia total de método, la frustración más cruda de los tres. También se enteró tarde u olvidó una entrega. No completó las preguntas de funcionalidad más útil ni de dudas. | "Se complica coordinar con otras personas": la fricción no es solo personal sino de coordinación grupal. También se enteró tarde u olvidó una entrega. Le preocupa la privacidad: "que solicite información privada sin un motivo claro". |
| **Contexto de uso** | Consulta MIEL, mail y calendario desde ambos dispositivos. No se queda sin buena conexión. | Consulta desde ambos dispositivos. Es el único que a veces se queda sin buena conexión al revisar cosas de la facultad. Sí usaría el check-in. | Consulta desde ambos dispositivos. No se queda sin buena conexión. Sí usaría el check-in. |

Los tres atribuyen sus momentos de sobrecarga a la combinación de responsabilidades y no a una sola de ellas, incluido U3, que no trabaja actualmente. Ninguno de los tres registra hoy en ningún lado su estado de ánimo o su nivel de estrés.

## Hipótesis de valor

**Creemos que** los estudiantes de 4to año de Ingeniería Informática en la UNLaM que cursan una carga completa de materias (6 en los tres casos relevados) y combinan la cursada con trabajo de varias horas diarias, o con una exigencia académica igualmente intensa aunque no trabajen,

**tienen el problema de** organizar sus entregas y evaluaciones de forma dispersa e informal (WhatsApp, agenda del celular, o directamente sin ningún método), lo que les genera enterarse tarde u olvidarse de entregas y parciales, y sentir con frecuencia más responsabilidades de las que pueden manejar sin tener ningún registro de su propio estado de ánimo o nivel de estrés que les permita anticiparlo,

**nuestra solución es** A.N.A.N.A., una app que centraliza materias, entregas y eventos en una vista semanal agrupada por prioridad (la forma que los tres usuarios relevados prefirieron por sobre una lista plana), sumando un check-in breve y privado de bienestar que dispara alertas preventivas cuando se acumulan tareas y carga,

**y sabremos que estamos en lo correcto cuando** durante la prueba del MVP la mayoría de los usuarios reemplacen efectivamente su método actual por A.N.A.N.A. en vez de usarla como algo adicional, tal como los tres manifestaron que harían, y al menos 2 de cada 3 completen el check-in de bienestar de forma sostenida a lo largo de la prueba.

## Estado de los supuestos del TP1

| Supuesto del TP1 | Estado | Evidencia |
|---|---|---|
| **1.** Combinar estudio, trabajo o responsabilidades familiares reduce el tiempo disponible y aumenta la percepción de sobrecarga. | **Confirmado** | Los tres usuarios sienten con frecuencia más responsabilidades de las que pueden manejar, y los tres lo atribuyen a "combinación", incluido U3, que no trabaja actualmente. |
| **2.** Una vista semanal con prioridades resulta más útil que una lista plana de tareas. | **Confirmado** | Los tres usuarios, sin excepción, prefieren la vista agrupada por día con prioridad. |
| **3.** La mayoría accederá principalmente desde el teléfono celular. | **Refutado** | Los tres respondieron "ambos" dispositivos, sin preferencia marcada por el celular. |
| **4.** Los estudiantes realizarán un check-in periódico si demora menos de dos minutos y sus respuestas son privadas. | **Confirmado** | U2 y U3 sí lo usarían. U1 no, pese a no tener objeciones al resto de la propuesta. |
| **5. CRÍTICO.** Las herramientas actuales no resuelven de manera conjunta la organización académica y el seguimiento del bienestar, y los estudiantes probarían una solución unificada. | **Confirmado** | Ninguno usa hoy algo integrado (WhatsApp, ninguna, agenda del celular) y ninguno registra su ánimo. Los tres reemplazarían su método actual por A.N.A.N.A. |

### Implicancia del Supuesto 3 refutado

Es el cambio de mayor impacto para el diseño. El producto no puede concebirse como una aplicación exclusivamente móvil: debe ser igualmente usable en computadora, porque los usuarios alternan entre ambos dispositivos según el momento. Además, U2 es el único que a veces se queda sin buena conexión, lo cual sugiere evaluar un comportamiento razonable ante conectividad intermitente, aunque con un solo caso no alcanza para convertirlo en requisito.

### Implicancia del supuesto crítico confirmado

El valor diferencial no está en una funcionalidad aislada sino en la propuesta unificada. El MVP debe mostrar esa integración desde el primer uso, en lugar de presentar la organización académica y el check-in de bienestar como dos herramientas separadas.

## Hallazgos nuevos, no previstos en ningún supuesto

1. **Coordinación con otras personas.** U3 señaló "se complica coordinar con otras personas" como su principal fricción. Los supuestos del TP1 contemplaban únicamente la organización individual, no la coordinación grupal. Queda registrado como necesidad detectada, fuera del alcance de esta iteración.
2. **La barrera del check-in es de confianza, no de tiempo.** U3 planteó como duda concreta "que solicite información privada sin un motivo claro", y U1 rechazó puntualmente el check-in aunque no tenía reparos con el resto del producto. La privacidad del check-in necesita explicarse, no alcanza con que sea rápido.
3. **Punto de partida más bajo de lo previsto.** U2 respondió "no tengo organización": no parte de una herramienta imperfecta sino de ninguna herramienta. El producto debe funcionar también para quien no tiene ningún método previo que reemplazar.
