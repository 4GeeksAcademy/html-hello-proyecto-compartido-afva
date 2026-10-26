# SPEC-001 — Home | Fashion Store

**Proyecto:** Fashion Store — prototipo colaborativo de e-commerce  
**Vista:** `index.html`  
**Estado:** Propuesta pendiente de aprobación  
**Fuente:** Enunciado «Mi primer proyecto profesional colaborativo» de 4Geeks Academy.

## 1. Objetivo

Crear la página de inicio de un prototipo de tienda online para una marca de ropa con sede en Francia. La Home debe presentar la marca y sus productos, permitir navegar a las otras vistas y demostrar un diseño moderno, coherente, accesible y responsive.

## 2. Alcance

**Incluye:** navbar, hero, dos listados horizontales de productos (nuevos lanzamientos y más vendidos), footer, enlaces entre vistas, SEO y datos estructurados adecuados.

**No incluye:** motor de búsqueda real, autenticación, lógica de carrito, backend, pagos, filtros dinámicos ni JavaScript personalizado.

**Tecnologías autorizadas:** HTML5 y Tailwind CSS exclusivamente. Se admite la carga de Tailwind por CDN si ya es la convención acordada del repositorio. El JSON-LD de Schema.org es dato estructurado, no lógica JavaScript ejecutable.

## 3. Requisitos funcionales

| ID | Requisito | Criterio de aceptación |
|---|---|---|
| RF-001 | Estructura general | `index.html` incluye `header`, `main` y `footer`, con un único `h1`. |
| RF-002 | Navbar compartida | Muestra logo/nombre de marca, barra de búsqueda y acceso visual a cuenta de usuario; contiene navegación a las vistas principales. |
| RF-003 | Hero | Presenta campaña o productos destacados con título, texto y CTA enlazado a `catalog.html`. |
| RF-004 | Nuevos lanzamientos | Incluye sección identificable con tarjetas de producto dispuestas horizontalmente en escritorio y adaptadas a móvil. |
| RF-005 | Más vendidos | Incluye una segunda sección identificable con tarjetas de producto dispuestas horizontalmente en escritorio y adaptadas a móvil. |
| RF-006 | Tarjetas de producto | Cada tarjeta presenta imagen con `alt`, nombre, precio de ejemplo y enlace a `product.html`. |
| RF-007 | Footer compartido | Contiene categorías (calzado, camisas, pantalones, accesorios), legal (términos y condiciones, privacidad, sobre la marca) y contacto. |
| RF-008 | Navegación entre vistas | La Home enlaza a `catalog.html`, `product.html`, `cart.html` y `checkout.html` donde resulte apropiado, sin enlaces rotos al finalizar la integración. |
| RF-009 | Coherencia entre vistas | Navbar y footer de la Home establecen una estructura y estilos acordados que se reutilizarán en las otras cuatro páginas. |

**Aclaraciones funcionales:**

- La barra de búsqueda será visual y accesible, pero no realizará búsquedas: no debe simular resultados inexistentes. Si se presenta como formulario, se documentará claramente su carácter demostrativo y no se enviará a un destino ficticio.
- El acceso a cuenta de usuario será un elemento visual sin autenticación real. No se inventará una página de cuenta fuera del alcance aprobado.
- Los enlaces legales y de contacto deben apuntar a destinos existentes y aprobados; si no existen, se mostrarán como texto informativo sin enlaces falsos.
- Los productos, precios y campañas serán datos ficticios de demostración, identificados como tales en el proyecto; deben ser coherentes con catálogo y producto.

## 4. Requisitos no funcionales

| ID | Requisito | Criterio de aceptación |
|---|---|---|
| RNF-001 | Responsive mobile-first | Se visualiza correctamente en móvil, tablet y escritorio, sin desbordamiento horizontal. |
| RNF-002 | Tailwind | Los estilos se construyen con utilidades Tailwind, sin frameworks adicionales. |
| RNF-003 | HTML semántico | Uso correcto de `header`, `nav`, `main`, `section`, `article` cuando proceda y `footer`. |
| RNF-004 | Accesibilidad | Imágenes con `alt`, búsqueda con etiqueta accesible, foco visible, contraste legible y navegación por teclado. |
| RNF-005 | SEO | `title`, `meta description`, jerarquía de encabezados, contenido textual indexable y enlaces descriptivos. |
| RNF-006 | Schema.org | Datos estructurados válidos y ajustados a información confirmada (por ejemplo `Organization`); sin datos inventados. |
| RNF-007 | Consistencia visual | Tipografía, colores, espaciados y estilos de tarjetas acordados y documentados para el equipo. |
| RNF-008 | Restricción tecnológica | Sin React, Vue, Angular, backend ni JavaScript personalizado. |
| RNF-009 | Colaboración | Cambios realizados en rama de funcionalidad y revisados mediante Pull Request según el flujo Git acordado. |

## 5. Contenido mínimo

1. **Navbar:** marca/logo, búsqueda, cuenta, navegación hacia catálogo y carrito.
2. **Hero:** campaña o selección destacada, CTA «Ver catálogo» (texto provisional).
3. **Nuevos lanzamientos:** tarjetas con imagen, nombre, precio y enlace a producto.
4. **Más vendidos:** tarjetas con los mismos elementos.
5. **Footer:** categorías indicadas, textos legales y contacto sin inventar datos.

Para esta Home se aprobaron diez espacios numerados en «Más vendidos» y ninguno en «Nuevos lanzamientos»; esta última sección muestra «Próximamente» hasta que se definan productos. Los espacios reservados no equivalen a tarjetas de producto completas. El requisito de 20 productos corresponde a la vista **Catálogo**, no a la Home.

### Contenido del hero

- **Marca / identidad principal:** MAISON NOVA, aprobada según `docs/design-system.md`.
- **Titular de campaña:** pendiente de aprobación. El nombre de marca que aparece como `h1` no sustituye un titular de campaña aprobado.
- **Texto de campaña:** pendiente de aprobación. El texto actualmente mostrado en `index.html` es provisional y no debe considerarse contenido final.
- **Imagen de campaña:** recurso pendiente de aprobación. `index.html` muestra únicamente un espacio reservado, no una imagen de campaña.
- **CTA:** enlace a `catalog.html`; el texto visible «Ver colección» es provisional hasta aprobar el contenido final del hero.

El layout del hero ya está implementado en `index.html`. T-005 permanece pendiente hasta aprobar el titular, el texto y la imagen, y reemplazar los marcadores provisionales.

## 6. Dependencias y decisiones pendientes

- **Marca e idioma:** identidad provisional MAISON NOVA, logotipo tipográfico, estilo e idioma español aprobados; consultar `docs/design-system.md`.
- **Productos:** imágenes autorizadas, nombres, precios, moneda y cantidad de tarjetas por sección.
- **Hero:** titular, texto e imagen de campaña aún pendientes de aprobación.
- **Contacto y legal:** no se proporcionaron datos de contacto ni destinos legales; se mostrarán sin enlaces ni datos inventados según el sistema de diseño aprobado.
- **Navegación común:** estructura y enlaces aprobados; consultar `docs/design-system.md`.
- **Rutas:** confirmadas como `catalog.html`, `product.html`, `cart.html` y `checkout.html`.

No bloquear la estructura semántica por datos pendientes, pero solicitar aprobación antes de publicar contenido o identidad visual inventados.

## 7. Criterios de aceptación global

- [ ] Todos los RF-001 a RF-009 están implementados o sus limitaciones demostrativas están documentadas.
- [ ] Todos los RNF-001 a RNF-009 han sido revisados.
- [ ] Home comprobada visualmente a 375 px, 768 px y 1440 px como referencias de prueba.
- [ ] Enlaces y navegación por teclado comprobados en navegador.
- [ ] Contenido coherente con las otras vistas y sin funcionalidades falsas.
- [ ] Cambios revisados mediante Pull Request antes de integrarlos en `develop`.

## 8. Fuera de alcance

No implementar lógica de búsqueda, login, catálogo dinámico, selección de talla, estado de carrito, checkout real ni procesamiento de pagos. Estas funciones exceden HTML + Tailwind y el alcance de la Home.
