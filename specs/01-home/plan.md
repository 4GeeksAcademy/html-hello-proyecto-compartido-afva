# PLAN-001 — Implementación de la Home | Fashion Store

**Referencia:** `specs/01-home/spec.md` (SPEC-001)  
**Archivo principal:** `index.html`  
**Estado:** Propuesta pendiente de aprobación

## 1. Estrategia

Implementar una Home estática, semántica y mobile-first con HTML5 y Tailwind CSS, sin dependencias de aplicación ni JavaScript personalizado. Reutilizar las convenciones del repositorio y coordinar la navbar/footer con el resto del equipo.

## 2. Inspección previa

1. Leer `README.md`, `CONTEXT.md` y `AGENTS.md` si existen.
2. Inspeccionar la plantilla HTML y los recursos existentes; no sobrescribir trabajo previo sin autorización.
3. Confirmar rutas reales de las cinco páginas y convención de carga de Tailwind.
4. Revisar los elementos visuales compartidos acordados por el equipo.
5. Identificar decisiones abiertas de SPEC-001 antes de crear contenido de marca.

## 3. Estructura propuesta de `index.html`

```text
<!DOCTYPE html>
html[lang]
├── head
│   ├── charset, viewport, title, meta description
│   ├── Tailwind CSS (según convención del repositorio)
│   └── JSON-LD Schema.org con datos confirmados
└── body
    ├── header
    │   ├── marca/logo
    │   ├── búsqueda demostrativa y accesible
    │   ├── cuenta (presentación visual)
    │   └── nav (enlaces reales)
    ├── main
    │   ├── hero (h1 + CTA al catálogo)
    │   ├── section#new-arrivals (tarjetas)
    │   └── section#best-sellers (tarjetas)
    └── footer
        ├── categorías
        ├── legal
        └── contacto
```

## 4. Diseño y responsive

- **Mobile-first:** una columna para el hero y tarjetas en una distribución legible; barra de navegación que se adapte sin menú desplegable dependiente de JavaScript.
- **Tablet:** ajustar espaciados y número de tarjetas visibles mediante `md:`.
- **Escritorio:** hero más amplio y tarjetas en filas horizontales mediante `lg:`; evitar desbordamientos.
- Aplicar estilos de foco `focus-visible:` y contraste suficiente.
- Reutilizar colores, tipografía y componentes visuales acordados; no introducir una identidad de marca definitiva sin aprobación.

## 5. Estrategia de contenido y enlaces

- Usar contenido de muestra únicamente cuando el equipo apruebe los textos, imágenes y precios.
- Las tarjetas enlazan a `product.html` como vista de producto demostrativa; no afirmar que cada tarjeta tiene una página específica.
- El CTA principal enlaza a `catalog.html`.
- La navegación ofrece acceso a catálogo y carrito; checkout se alcanza normalmente desde carrito.
- La búsqueda y cuenta se representan sin fingir funcionalidades no implementadas.
- Para legal/contacto, utilizar enlaces solo si existen destinos reales; de lo contrario, texto sin enlaces falsos y registrar la limitación.

## 6. SEO, Schema.org y accesibilidad

- Un único `h1`; `h2` para ambas secciones de productos.
- `title` y `meta description` específicos de la Home.
- Imágenes con `alt` descriptivo; imágenes decorativas con `alt=""` cuando corresponda.
- Etiquetado accesible para búsqueda y enlaces con nombres comprensibles.
- JSON-LD de `Organization` o tipo pertinente, con propiedades verificadas. No incluir datos de empresa, URL o dirección inventados.
- Verificar navegación por teclado y foco visible manualmente en navegador.

## 7. Archivos y responsabilidades

| Archivo | Acción prevista |
|---|---|
| `index.html` | Implementar Home. |
| `assets/images/` | Reutilizar imágenes existentes aprobadas; añadir nuevas solo con autorización. |
| `README.md` | Modificar solo si es necesario documentar ejecución o limitaciones y está autorizado. |
| `specs/01-home/tasks.md` | Registrar avance y evidencias después de verificar. |

**Importante:** con HTML estático no existe un mecanismo de componentes compartidos: navbar y footer deberán replicarse de forma consistente en las otras vistas, coordinando cualquier cambio con el equipo.

## 8. Validación

1. **Estructura:** DOCTYPE, idioma, metadatos, un `h1`, regiones semánticas y enlaces.
2. **Responsive:** inspección manual a 375, 768 y 1440 px; comprobar que no hay scroll horizontal inesperado.
3. **Contenido:** dos secciones de tarjetas, imágenes, nombres, precios y enlaces a producto.
4. **Accesibilidad:** teclado, foco, `alt`, etiquetas y contraste.
5. **SEO:** metadatos y JSON-LD parseable con propiedades confirmadas.
6. **Navegación:** comprobar rutas entre las cinco vistas cuando existan.
7. **Restricción tecnológica:** confirmar que no se ha añadido JavaScript personalizado, frameworks ni backend.
8. **Colaboración:** revisar diff, preparar PR desde `feature/home` a `develop` según aprobación.

Si una verificación no puede ejecutarse, marcarla como **no verificada**, nunca como superada.

## 9. Riesgos y mitigaciones

| Riesgo | Mitigación |
|---|---|
| Falta de identidad de marca | Solicitar decisión; no inventar identidad definitiva. |
| Búsqueda/cuenta sin JavaScript | Presentación demostrativa, sin acciones engañosas. |
| Cambios simultáneos en navbar/footer | Acordar estructura y estilos comunes antes de desarrollar vistas en paralelo. |
| Imágenes o precios inconsistentes | Definir datos de muestra compartidos antes de poblar tarjetas. |
| Enlaces legales inexistentes | Evitar `href="#"`; documentar destinos pendientes. |
| SEO con datos ficticios | Usar únicamente propiedades confirmadas en Schema.org. |

## 10. Condición para empezar

Aprobar SPEC-001 y este PLAN-001, resolver decisiones que afecten al contenido de marca y autorizar expresamente la primera tarea de implementación. No realizar commits ni push sin aprobación.
