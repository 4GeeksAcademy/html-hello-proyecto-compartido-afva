# Instrucciones para agentes de IA

## Memory Bank

- Al iniciar cada tarea, consulta `memory-bank/decisions.md` y `memory-bank/progress.md` si existen.
- Consulta también `CONTEXT.md`, `README.md` y los documentos SPEC, PLAN y TASKS aplicables. Lee `docs/design-system.md` para decisiones de identidad, interfaz o contenido visual.
- Trata el Memory Bank como un resumen con referencias, no como sustituto de las especificaciones. Comprueba los archivos fuente cuando haya discrepancias y distingue hechos verificados, decisiones aprobadas y pendientes.
- Actualiza `memory-bank/progress.md` cuando haya avances relevantes o nuevas verificaciones; registra evidencias y no marques trabajo como completado sin comprobarlo.
- Actualiza `memory-bank/decisions.md` cuando se aprueben decisiones técnicas, arquitectónicas, visuales o de producto importantes. Incluye una justificación breve y referencias a la fuente detallada.
- Evita duplicar en el Memory Bank requisitos, planes o instrucciones ya mantenidos en otros documentos; resume el estado y enlaza la fuente correspondiente.

## Antes de trabajar

- Lee `CONTEXT.md`, `README.md` y los documentos SDD aplicables a la tarea antes de empezar. Si falta una especificación necesaria, indícalo y solicita aclaración; no infieras requisitos.
- Revisa el estado de Git antes de modificar archivos. Identifica cambios existentes y consérvalos; nunca sobrescribas el trabajo de otras personas.
- Confirma el alcance autorizado y modifica únicamente los archivos necesarios para la tarea.

## Tecnologías y calidad

- Usa exclusivamente HTML5 y Tailwind CSS.
- No introduzcas JavaScript personalizado, frameworks frontend, backend, dependencias adicionales ni otras tecnologías sin autorización explícita.
- Aplica HTML semántico, buenas prácticas de SEO, Schema.org, accesibilidad y diseño mobile-first adaptable a móvil, tablet y escritorio.

## Flujo de trabajo

- Antes de implementar cada funcionalidad, sigue el flujo SDD: **SPEC → PLAN → TASKS → implementación**. Valida la implementación frente a las tareas y especificación aprobadas.
- Implementa únicamente tareas expresamente autorizadas. Si una tarea, requisito o decisión de arquitectura o diseño no está definido, detente y solicita aprobación.
- No crees ramas, hagas commits, merges ni push sin autorización explícita.
- Al finalizar, verifica los cambios y comunica qué se hizo, cómo se validó, las limitaciones y cualquier bloqueo.
