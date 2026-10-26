# Contexto del proyecto

## Cliente y objetivo

Proyecto formativo de 4Geeks Academy. Una consultora debe desarrollar un prototipo de tienda online para una marca de ropa con sede en Francia. La marca provisional y las decisiones generales de diseño están documentadas en [`docs/design-system.md`](docs/design-system.md); el catálogo de productos aún está pendiente.

## Continuidad entre iteraciones

- Al iniciar una tarea, consulta [`memory-bank/decisions.md`](memory-bank/decisions.md) para conocer las decisiones aprobadas y [`memory-bank/progress.md`](memory-bank/progress.md) para el estado verificado, los pendientes y las evidencias.
- El Memory Bank es un resumen de continuidad, no reemplaza las fuentes del proyecto: `AGENTS.md` contiene instrucciones de trabajo; `CONTEXT.md`, el alcance y las restricciones generales; `docs/design-system.md`, la identidad y las reglas visuales; y los archivos `spec.md`, `plan.md` y `task.md` de cada vista, sus requisitos y tareas.
- Si el Memory Bank, el README o una implementación parecen contradecir una fuente aprobada, comprueba los documentos fuente y el código. Distingue decisiones aprobadas de estados verificados y pendientes; no infieras requisitos.
- Después de avances relevantes, actualiza `progress.md` con evidencias. Registra en `decisions.md` las decisiones importantes solo cuando hayan sido aprobadas. Evita duplicar allí el contenido detallado de las specs y planes.

## Alcance

El prototipo comprende cinco vistas:

1. Home
2. Catálogo
3. Producto
4. Carrito
5. Checkout

Este alcance identifica las vistas, pero no presupone flujos, contenido, productos ni funcionalidades que no estén especificados.

## Requisitos transversales

- Considerar SEO en la estructura y el contenido de las páginas.
- Usar HTML semántico.
- Incorporar Schema.org.
- Aplicar un diseño moderno y adaptable a móvil, tablet y escritorio.

## Tecnologías permitidas

Usar exclusivamente HTML5 y Tailwind CSS. No utilizar React, Vue, Angular, backend ni JavaScript personalizado. Tailwind CSS se limita a la presentación; no habilita por sí solo lógica de aplicación.

## Requisitos por vista

El README ofrece una descripción general del proyecto y puede no reflejar las decisiones más recientes. Los requisitos específicos de cada vista se mantienen en su documentación SDD aplicable. Actualmente, Home tiene documentos en `specs/01-home/`; para las demás vistas, consulta sus propios documentos antes de implementar y confirma cualquier requisito que no esté especificado.

| Vista | Alcance conocido | Detalles específicos del ejercicio |
| --- | --- | --- |
| Home | Vista inicial de la tienda. | `specs/01-home/spec.md`, `plan.md` y `task.md`. Consultar también el estado verificado en `memory-bank/progress.md`. |
| Catálogo | Vista de catálogo de la tienda. | Consultar la SPEC/PLAN/TASKS aplicables antes de implementar; no inferir requisitos. |
| Producto | Vista de producto. | Consultar la SPEC/PLAN/TASKS aplicables antes de implementar; no inferir requisitos. |
| Carrito | Vista del carrito. | Consultar la SPEC/PLAN/TASKS aplicables antes de implementar; no inferir requisitos. |
| Checkout | Vista de checkout. | Consultar la SPEC/PLAN/TASKS aplicables antes de implementar; no inferir requisitos. |

No se deben inferir requisitos adicionales hasta disponer de la especificación del ejercicio.

## Límites del prototipo

Al estar restringido a HTML y Tailwind CSS, el prototipo puede representar las vistas y su presentación, pero no implementar lógica dinámica o persistente. En particular, no puede mantener un carrito funcional entre páginas, recalcular importes, procesar pagos ni enviar pedidos. Cualquier interacción que requiera JavaScript personalizado o un backend queda fuera del alcance indicado.

## Metodología de desarrollo

Seguir Spec-Driven Development en este orden:

1. **SPEC:** acordar y documentar los requisitos.
2. **PLAN:** definir el enfoque y la secuencia de trabajo.
3. **TASKS:** dividir el plan en tareas concretas.
4. **Implementación:** construir lo especificado con las tecnologías permitidas.
5. **Validación:** comprobar los requisitos acordados en las cinco vistas y los tamaños de pantalla objetivo.

Si la especificación del ejercicio no está disponible, aclarar los requisitos pendientes antes de implementarlos.

## Colaboración mediante Git

- Trabajar en ramas dedicadas para los cambios, manteniendo la rama principal estable.
- Crear commits pequeños, enfocados y con mensajes descriptivos.
- Proponer los cambios mediante Pull Requests (PR), indicando su alcance y cómo se validaron.
- Revisar el código de cada PR antes de integrarlo; resolver observaciones y comprobar que los cambios respetan la especificación y las tecnologías permitidas.

## Decisiones pendientes

- Catálogo de productos y su contenido.
- Distribución del trabajo entre las personas del equipo.
- Requisitos detallados y decisiones de las vistas distintas de Home, según sus documentos SDD aplicables.
