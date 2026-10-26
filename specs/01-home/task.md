# TASKS-001 — Home | Fashion Store

**Especificación:** `specs/01-home/spec.md` (SPEC-001)  
**Plan:** `specs/01-home/plan.md` (PLAN-001)  
**Estado:** Implementación parcial; pendiente aprobación del contenido del hero, contenido final de producto y validación manual

## Reglas de ejecución

- Ejecutar las tareas en orden, salvo cambio de dependencias aprobado.
- Marcar `[x]` solo después de verificar el resultado; registrar evidencias.
- Seguir `AGENTS.md`, `CONTEXT.md` y README aplicables.
- No sobrescribir trabajo de compañeros ni crear archivos adicionales sin autorización.
- No realizar commits, push o merges sin aprobación expresa.

## Fase 0 — Preparación

### T-001 — Inspeccionar el repositorio

- [x] Leer contexto, instrucciones y documentos SPEC-001 / PLAN-001.
- [x] Revisar `index.html`, rutas de las otras vistas y `assets/images/`.
- [x] Confirmar cómo se carga Tailwind y el estado de Git.
- [x] Enumerar archivos que se modificarán y pedir aprobación.

**Verificación:** inspección completada y alcance autorizado antes de implementar.  
**Requisitos:** RNF-008, RNF-009.

**Evidencia:** `index.html`, `catalog.html`, `product.html`, `cart.html` y `checkout.html` están vacíos; `assets/images/` no contiene recursos; no se encontró una convención de carga de Tailwind en los HTML. Rama activa: `home`. Archivos autorizados: `index.html`, este `task.md`, `CONTEXT.md` y `docs/design-system.md`.

### T-002 — Resolver contenido y diseño compartido

- [x] Confirmar nombre de marca, idioma, logo y línea visual.
- [x] Acordar con el equipo la estructura de navbar y footer.
- [x] Confirmar imágenes, nombres, precios y cantidad de tarjetas por sección (espacios reservados aprobados; contenido real pendiente).
- [x] Confirmar contenido legal/contacto y rutas existentes; registrar ausencias.

**Verificación:** decisiones aprobadas o bloqueos documentados.  
**Requisitos:** RF-002, RF-006, RF-007, RF-009, RNF-007.

**Decisiones registradas:** diez espacios numerados para más vendidos, con áreas reservadas para imagen y precio; no habrá tarjetas de nuevos lanzamientos por ahora y la sección mostrará «Próximamente». Nombres comerciales, imágenes, precios y moneda reales siguen pendientes. Esta excepción deja RF-004 pendiente hasta que se aprueben productos nuevos.

## Fase 1 — HTML y contenido

### T-003 — Crear estructura semántica y metadatos

- [x] Preparar `index.html` con DOCTYPE, idioma, `head`, `body`, `title` y `meta description`.
- [x] Añadir `header`, `main`, `footer` y un único `h1`.

**Verificación:** estructura HTML válida y jerarquía de encabezados correcta.  
**Requisitos:** RF-001, RNF-003, RNF-005.

**Evidencia:** HTML parseado con `html.parser`; un `h1`; metadatos presentes.

### T-004 — Implementar navbar

- [x] Mostrar marca/logo, búsqueda demostrativa y cuenta visual.
- [x] Incorporar navegación con enlaces reales a vistas disponibles.
- [x] Adaptar la disposición a móvil sin JavaScript.

**Verificación:** enlaces comprobados, navegación legible y accesible.  
**Requisitos:** RF-002, RF-008, RF-009.

**Evidencia:** enlaces locales comprobados contra archivos existentes; la búsqueda está deshabilitada y la cuenta es texto visual. La revisión manual de legibilidad y teclado queda pendiente.

### T-005 — Implementar hero

- [ ] Añadir campaña o productos destacados aprobados.
- [ ] Incorporar contenido aprobado: titular, descripción y CTA a `catalog.html`.

**Verificación:** pendiente hasta aprobar titular, texto e imagen de campaña; después comprobar CTA y contenido indexable.  
**Requisitos:** RF-003, RNF-005.

**Estado actual:** el layout está implementado en `index.html`; el texto y el espacio de imagen son provisionales y no cuentan como contenido aprobado.

### T-006 — Implementar nuevos lanzamientos

- [x] Crear sección con encabezado `h2`.
- [ ] Añadir tarjetas aprobadas con imagen, nombre, precio y enlace a `product.html`.
- [ ] Aplicar distribución horizontal adaptable.

**Verificación:** tarjetas y enlaces comprobados.  
**Requisitos:** RF-004, RF-006.

### T-007 — Implementar más vendidos

- [x] Crear sección diferenciada con encabezado `h2`.
- [ ] Añadir tarjetas aprobadas con imagen, nombre, precio y enlace a `product.html`.
- [x] Aplicar distribución horizontal adaptable.

**Verificación:** tarjetas y enlaces comprobados.  
**Requisitos:** RF-005, RF-006.

### T-008 — Implementar footer

- [x] Incluir categorías: calzado, camisas, pantalones, accesorios.
- [x] Incluir legal: términos y condiciones, privacidad, sobre la marca.
- [x] Incluir contacto con información confirmada, sin inventar datos ni enlaces.
- [x] Mantener la estructura compartida acordada con el equipo.

**Verificación:** tres bloques presentes y enlaces válidos si los hay.  
**Requisitos:** RF-007, RF-009.

## Fase 2 — Calidad técnica

### T-009 — Aplicar Tailwind y responsive

- [x] Aplicar estilos mobile-first y breakpoints responsive según necesidad.
- [x] Mantener consistencia visual entre hero, tarjetas, navbar y footer.
- [ ] Comprobar manualmente 375, 768 y 1440 px sin desbordamiento horizontal.

**Verificación:** revisión visual documentada por tamaño de pantalla.  
**Requisitos:** RNF-001, RNF-002, RNF-007.

### T-010 — Verificar accesibilidad

- [x] Revisar `alt`, etiquetas, landmarks y enlaces descriptivos.
- [ ] Probar navegación por teclado, foco visible y contraste.
- [x] Evitar controles que aparenten ejecutar funciones inexistentes.

**Verificación:** pruebas manuales y problemas documentados.  
**Requisitos:** RNF-003, RNF-004.

### T-011 — Completar SEO y Schema.org

- [x] Verificar título, descripción, encabezados y contenido indexable.
- [x] Añadir JSON-LD con datos de marca confirmados.
- [x] Comprobar sintaxis del JSON-LD y ausencia de datos inventados.

**Verificación:** comprobaciones de metadatos y JSON-LD.  
**Requisitos:** RNF-005, RNF-006.

## Fase 3 — Integración y cierre

### T-012 — Probar navegación e integración

- [ ] Abrir Home en navegador y comprobar recursos y enlaces.
- [ ] Verificar rutas con catálogo, producto, carrito y checkout cuando estén disponibles.
- [x] Comprobar que no se ha añadido JavaScript personalizado ni frameworks.
- [x] Registrar pruebas no ejecutadas o dependencias externas.

**Verificación:** resultados reproducibles y limitaciones documentadas.  
**Requisitos:** RF-008, RNF-008.

**Pendiente de ejecución:** no se realizó revisión visual en navegador ni comprobación manual a 375, 768 y 1440 px, navegación por teclado o contraste. Tailwind CSS v4 se carga desde su CDN aprobado.

### T-013 — Revisar y preparar Pull Request

- [ ] Contrastar RF y RNF con SPEC-001.
- [ ] Revisar `git diff` y archivos modificados.
- [ ] Presentar resumen de cambios, pruebas y pendientes.
- [ ] Solicitar autorización para commit/push y PR hacia `develop`.
- [ ] Obtener revisión del compañero antes de integrar.

**Verificación:** checklist completo, evidencias y revisión del PR.  
**Requisitos:** RNF-009.

## Matriz de trazabilidad

| Requisito | Tareas |
|---|---|
| RF-001 | T-003 |
| RF-002 | T-002, T-004 |
| RF-003 | T-005 |
| RF-004 | T-006 |
| RF-005 | T-007 |
| RF-006 | T-002, T-006, T-007 |
| RF-007 | T-002, T-008 |
| RF-008 | T-004, T-012 |
| RF-009 | T-002, T-004, T-008 |
| RNF-001 | T-009 |
| RNF-002 | T-009 |
| RNF-003 | T-003, T-010 |
| RNF-004 | T-010 |
| RNF-005 | T-003, T-005, T-011 |
| RNF-006 | T-011 |
| RNF-007 | T-002, T-009 |
| RNF-008 | T-001, T-012 |
| RNF-009 | T-001, T-013 |

**Cierre:** ninguna tarea se considera completada sin su verificación. Los bloqueos se registran explícitamente y no se ocultan marcando casillas.
