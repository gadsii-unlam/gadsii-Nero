# Brief de Producto

<!-- Versión 1 — TP1. Cada versión siguiente abre con un párrafo de qué cambió y por qué. -->

Esta es la primera versión del brief de producto. Se consolidó la información definida en el TP1 sobre el segmento elegido, el producto, sus funcionalidades principales, las integraciones previstas, los grupos de usuarios y los supuestos iniciales. Esta versión servirá como base para las próximas actualizaciones del brief a partir de la evidencia obtenida en los siguientes TP.

## Segmento elegido

El segmento elegido está compuesto por estudiantes regulares de carreras de pregrado y grado de la UNLaM que, debido al trabajo, responsabilidades familiares, o cualquier otro motivo personal, experimentan ansiedad, estrés, posible sobrecarga emocional y dificultades recurrentes de organización y rendimiento académico.

La evaluación externa de la UNLaM registra un universo total de 43.865 estudiantes. Como todavía no existe una medición institucional que cruce cursada, trabajo, responsabilidades, y situación emocional, estimamos inicialmente que el segmento podría representar entre el 20 % y el 35 % de ese universo, es decir, aproximadamente entre 9.000 y 15.000 estudiantes. Esta cifra es una estimación de trabajo y deberá revisarse con la evidencia obtenida en el TP2.

Elegimos este segmento porque enfrenta un problema concreto y frecuente: la coordinación de materias, fechas de entrega, evaluaciones, trabajo y responsabilidades personales puede generar olvidos, dificultad para establecer prioridades y una experiencia negativa en los estudiantes.

## Producto

### Nombre

El producto se denomina **A.N.A.N.A.: Ayuda y Notificaciones Académicas con Navegación Asistida**.

### Problema que resuelve

A.N.A.N.A. resuelve la dificultad de los estudiantes para centralizar sus obligaciones académicas, determinar prioridades y advertir tempranamente situaciones personales de sobrecarga.

La aplicación les ofrece un espacio privado donde pueden registrar materias, entregas, eventos y su estado general, obteniendo una vista integrada de su semana.

A.N.A.N.A. es una herramienta preventiva. No realiza diagnósticos clínicos, no interpreta enfermedades y no reemplaza la asistencia de profesionales de la salud.

### A quién le resuelve el problema

El producto está dirigido principalmente a los estudiantes del segmento seleccionado, es decir, estudiantes regulares de carreras de pregrado y grado de la UNLaM que combinan la cursada con trabajo, responsabilidades familiares o cualquier otro motivo personal y presentan dificultades de organización y rendimiento académico, ansiedad, estrés o posible sobrecarga emocional.

## Funcionalidades core

1. **Organización de materias, entregas y eventos.**
   El estudiante puede registrar las materias que cursa, fechas de entrega, evaluaciones y otros compromisos académicos.

2. **Dashboard y checklist semanal.**
   La plataforma genera una vista de las actividades pendientes, las prioridades y el progreso de la semana a partir de los datos reales cargados por el estudiante.

3. **Check-in de bienestar.**
   El estudiante puede registrar periódicamente su estado de ánimo, nivel de energía, estrés y carga percibida mediante una interacción breve y privada.

4. **Detección preventiva de sobrecarga.**
   La aplicación relaciona la cercanía de las obligaciones con los check-ins y presenta advertencias preventivas cuando identifica una acumulación de tareas o niveles elevados de carga.

5. **Relevamiento de estadísticas.**
   Usuarios administradores de la universidad pueden tener acceso a estadísticas anónimas de niveles promedio de sobrecargada, principales motivos y observaciones desglosados por carrera.

6. **Acceso a canales de ayuda.**
   El usuario puede acceder a diversos canales de comunicación proporcionados por la universidad para pedir asistencia.

## Integraciones previstas

* **Supabase Auth:** permite registrar usuarios, iniciar sesión y administrar identidades sin almacenar contraseñas directamente en la aplicación.
* **Supabase PostgreSQL:** proporciona persistencia para perfiles, materias, entregas, eventos y check-ins.
* **Formato iCalendar:** previsto para una etapa posterior, permitiría importar o exportar fechas con calendarios personales, siempre mediante autorización explícita del usuario.
* **Canales institucionales de apoyo:** integración futura. Cualquier incorporación de información o derivación institucional se realizará únicamente después de validar responsables, datos y protocolos con la UNLaM.

El producto requiere un front-end y un back-end de desarrollo propio. La interfaz, la lógica del dashboard, el checklist, el cálculo preventivo de sobrecarga, las validaciones y las operaciones sobre los datos son desarrollados por el equipo utilizando Next.js, React, TypeScript y Server Actions.

## Grupos de usuarios

### Estudiantes del segmento seleccionado

Son estudiantes regulares que combinan la cursada con trabajo o responsabilidades familiares y necesitan organizar obligaciones provenientes de distintos espacios. Se encuentran directamente afectados por el problema y utilizarían A.N.A.N.A. para planificar, establecer prioridades y registrar su nivel de carga.

Este es el **grupo de usuarios primario**. Fue elegido porque es quien experimenta el problema, carga los datos y recibe el valor principal de la solución.

La elección del usuario primario es **todavía hipotética** y deberá validarse mediante el relevamiento y las pruebas previstas.

### Equipos universitarios de bienestar y acompañamiento

Incluye profesionales y áreas institucionales vinculadas con bienestar estudiantil, orientación y acompañamiento de trayectorias. Podrían utilizar indicadores agregados y anónimos para reconocer tendencias generales. No accederían a check-ins ni datos personales de estudiantes individuales.

### Autoridades y responsables institucionales

Son las personas que podrían evaluar la implementación de la plataforma en la Universidad. Su motivación sería contar con una herramienta preventiva que contribuya a la permanencia y al bienestar estudiantil. Las decisiones institucionales deberían basarse en información real y anonimizada proveniente de A.N.A.N.A.

## Supuestos

### Supuesto 1

**Asumimos que combinar estudio, trabajo o responsabilidades familiares reduce el tiempo disponible para planificar y aumenta la percepción de sobrecarga.**

Se comprobará mediante entrevistas y un registro breve de actividades durante una semana, comparando responsabilidades, tiempo disponible y momentos de mayor carga.

### Supuesto 2

**Asumimos que una vista semanal con prioridades resulta más útil que una lista plana de tareas.**

Se comprobará mostrando ambas alternativas durante el relevamiento y observando cuál permite identificar con mayor rapidez la próxima actividad importante.

### Supuesto 3

**Asumimos que la mayoría de los estudiantes accederá a A.N.A.N.A. principalmente desde el teléfono celular.**

Se comprobará preguntando qué dispositivo utilizan para consultar MIEL, mensajes, calendarios y tareas, y mediante la prueba del MVP en diferentes tamaños de pantalla.

### Supuesto 4

**Asumimos que los estudiantes realizarán un check-in periódico si demora menos de dos minutos y sus respuestas son privadas.**

Se comprobará en la prueba del MVP midiendo cuántos usuarios completan el check-in, cuánto tardan y qué nivel de confianza expresan respecto del tratamiento de sus datos.

### Supuesto 5 — CRÍTICO

**Asumimos que las herramientas que actualmente utiliza el segmento no resuelven de manera conjunta y satisfactoria la organización académica y el seguimiento preventivo del bienestar, y que los estudiantes estarían dispuestos a probar una solución unificada.**

Se comprobará reconstruyendo el proceso actual de U1, U2 y U3, identificando problemas concretos y registrando su intención de uso. Luego se contrastará esa intención con el uso efectivo durante la prueba del MVP.

Este es el supuesto crítico porque, si los estudiantes ya resolvieran satisfactoriamente el problema o no consideraran valiosa una herramienta unificada, A.N.A.N.A. perdería su principal razón de ser.
