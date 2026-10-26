# Fashion Store | Prototipo de e-commerce

## 1. Descripción del proyecto
Proyecto colaborativo desarrollado como parte del curso de AI Engineering de 4Geeks Academy.

El objetivo es construir un prototipo visual de una tienda online para una marca de ropa con sede en Francia.

El prototipo debe ofrecer una experiencia moderna, consistente y responsive, aplicando buenas prácticas de desarrollo web, SEO, accesibilidad y colaboración mediante Git.

## 2. Objetivos

- Desarrollar cinco vistas principales de un e-commerce.
- Crear una identidad visual coherente en todas las páginas.
- Garantizar un diseño responsive para móvil, tablet y escritorio.
- Aplicar HTML semántico y buenas prácticas SEO.
- Incorporar datos estructurados Schema.org cuando corresponda.
- Practicar el desarrollo colaborativo mediante Git, ramas y Pull Requests.
- Utilizar Spec-Driven Development (SDD) para organizar el trabajo.

## 3. Alcance funcional

### 3.1 Home (`index.html`)

- Navbar con logo, búsqueda y menú de cuenta.
- Hero para campañas y productos destacados.
- Sección de nuevos lanzamientos.
- Sección de productos más vendidos.
- Footer con categorías, información legal y contacto.

### 3.2 Catálogo (`catalog.html`)

- Navbar y footer comunes.
- Filtros por categoría y talla.
- Rejilla de referencia de 4 columnas y 5 filas, con 20 productos.
- Enlaces a las páginas de producto.

### 3.3 Producto (`product.html`)

- Imagen principal del producto.
- Nombre, referencia y precio.
- Selección de talla y cantidad.
- Botón para agregar al carrito.
- Descripción detallada, materiales y usos recomendados.

### 3.4 Carrito (`cart.html`)

- Vista completa del carrito.
- Tres productos de ejemplo.
- Miniaturas, precios, cantidades y totales por producto.
- Resumen con subtotal, impuestos y total.
- Botón para acceder al checkout.

### 3.5 Checkout (`checkout.html`)

Formulario de pago dividido visualmente en tres pasos:

1. Datos personales.
2. Dirección de entrega.
3. Datos de pago con tarjeta.

El checkout será demostrativo. No procesará pagos reales ni almacenará información bancaria.

## 4. Tecnologías

| Tecnología | Uso |
| --- | --- |
| HTML5 | Estructura y contenido |
| Tailwind CSS | Diseño y responsive |
| Schema.org | Datos estructurados |
| Git | Control de versiones |
| GitHub | Repositorio y colaboración |
| GitHub Codespaces | Entorno de desarrollo |

**Restricción:** no utilizar React, Vue, Angular, JavaScript personalizado, backend ni frameworks adicionales.

Las interacciones que requieran lógica dinámica se representarán de forma demostrativa mediante HTML, sin simular funcionalidades que no estén implementadas.

## 5. Estructura del proyecto

```
fashion-store/
├── AGENTS.md
├── CONTEXT.md
├── README.md
├── index.html
├── catalog.html
├── product.html
├── cart.html
├── checkout.html
├── assets/
│   └── images/
└── specs/
    ├── 01-home/
    ├── 02-catalog/
    ├── 03-product/
    ├── 04-cart/
    └── 05-checkout/
```

Cada carpeta de `specs/` contendrá, cuando se defina su funcionalidad:

- `spec.md`: requisitos y criterios de aceptación.
- `plan.md`: estrategia técnica de implementación.
- `tasks.md`: tareas y verificaciones.

## 6. Metodología de desarrollo

Se utilizará Spec-Driven Development (SDD):

1. **Contexto:** comprender el proyecto, alcance y restricciones.
2. **SPEC:** definir qué debe construirse.
3. **PLAN:** determinar cómo se implementará.
4. **TASKS:** desglosar el trabajo en tareas verificables.
5. **Implementación:** desarrollar las tareas aprobadas.
6. **Validación:** comprobar requisitos, responsive, SEO y accesibilidad.

Los agentes de IA deberán seguir las instrucciones establecidas en `AGENTS.md`.

## 7. Colaboración mediante Git

### Estrategia de ramas

- `main`: versión estable del proyecto.
- `develop`: integración del trabajo de los desarrolladores.
- `feature/*`: ramas para funcionalidades individuales.

Ejemplos:

```
feature/home
feature/catalog
feature/product
feature/cart
feature/checkout
```

### Flujo de trabajo

1. Sincronizar la rama `develop`.
2. Crear una rama `feature/*`.
3. Desarrollar la funcionalidad asignada.
4. Verificar los cambios.
5. Realizar commits descriptivos.
6. Subir la rama a GitHub.
7. Crear un Pull Request hacia `develop`.
8. Solicitar revisión del otro desarrollador.
9. Integrar los cambios aprobados.

No se deben realizar cambios directamente sobre `main` durante el desarrollo habitual.

## 8. Convenciones de desarrollo

- Utilizar HTML5 semántico.
- Diseñar siguiendo un enfoque mobile-first.
- Aplicar Tailwind CSS de forma consistente.
- Utilizar etiquetas accesibles y textos alternativos en imágenes.
- Mantener títulos y metadescripciones adecuados en cada página.
- Utilizar nombres descriptivos para archivos y recursos.
- Mantener coherencia entre navbar, footer y navegación.
- Evitar dependencias innecesarias.
- No incluir información real de clientes o datos bancarios.

## 9. Ejecución del proyecto

El proyecto está formado por archivos HTML estáticos.

Para visualizarlo:

1. Abrir el repositorio en GitHub Codespaces o en un editor local.
2. Abrir `index.html` en un navegador, o servir la carpeta mediante un servidor estático disponible en el entorno.
3. Navegar entre las cinco vistas mediante sus enlaces.

No se requiere backend ni proceso de compilación.

## 10. Criterios generales de aceptación

- Las cinco vistas están implementadas y enlazadas.
- Navbar y footer presentan un diseño consistente.
- El sitio es responsive en móvil, tablet y escritorio.
- Se utiliza HTML semántico.
- Se aplican buenas prácticas de SEO y Schema.org.
- Los productos y precios de ejemplo mantienen coherencia entre vistas.
- El prototipo respeta la restricción tecnológica.
- El código está integrado y revisado mediante Git y Pull Requests.

## 11. Estado del proyecto

**Fase:** inicialización y preparación de la arquitectura.

Pendiente de definir:

- Nombre comercial de la marca.
- Identidad visual, colores y tipografía.
- Imágenes y productos de ejemplo.
- Reparto de responsabilidades entre los dos desarrolladores.
- Especificaciones y planes técnicos de cada vista.

## 12. Equipo

Proyecto desarrollado colaborativamente por dos participantes del curso de AI Engineering de 4Geeks Academy.

Las responsabilidades concretas se definirán antes de comenzar la implementación.
