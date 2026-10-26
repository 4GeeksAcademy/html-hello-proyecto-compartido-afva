# Decisions — MAISON NOVA

Last reviewed: 2026-10-26

This file is a concise record of approved project decisions, not a replacement for the specifications or implementation plan. Implementation evidence and outstanding work are in [progress.md](progress.md).

## Approved decisions

| Area | Decision | Rationale | Source |
| --- | --- | --- | --- |
| Technology | Use static HTML5 and Tailwind CSS only. Do not add custom JavaScript, frontend frameworks, backend services, or extra dependencies without explicit approval. | Keeps the prototype within its agreed technology limits; dynamic behavior must not be implied when it is not implemented. | [AGENTS.md](../AGENTS.md), [CONTEXT.md](../CONTEXT.md), [README.md](../README.md), [Home SPEC](../specs/01-home/spec.md) |
| Tailwind loading | The Home may load Tailwind CSS v4 through its browser CDN. | No existing project-wide loading convention was found, and CDN use was explicitly approved for the Home. | [Home tasks](../specs/01-home/task.md), [index.html](../index.html) |
| Development workflow | Follow SDD in order: SPEC → PLAN → TASKS → implementation and validation. Do not mark work complete without verification. | Maintains traceability and avoids treating assumptions as accepted requirements. | [AGENTS.md](../AGENTS.md), [CONTEXT.md](../CONTEXT.md), [Home tasks](../specs/01-home/task.md) |
| Current branch scope | Keep this iteration focused on Home; defer Catalog, Product, Cart, and Checkout to a later branch. Retain the approved Home placeholders for now. | Prevents unscoped work and avoids inventing content that has not been supplied. | User-approved scope; [progress](progress.md) |
| Brand | Provisional academic brand: MAISON NOVA, with a typographic wordmark. | Provides one approved identity for the prototype without asserting that it is a real commercial brand. | [Design system](../docs/design-system.md) |
| Visual direction | Minimal, editorial, contemporary; Spanish language; sans-serif typography; mobile-first. Colors: white `#FFFFFF`, near-black `#171717`, beige `#F5F1EB`. | An approved, reusable visual direction for the five views. | [Design system](../docs/design-system.md) |
| Shared navigation | Wordmark → `index.html`; “Colección” → `catalog.html`; “Carrito” → `cart.html`. “Mi cuenta” and search are visual-only; search does not execute. | Uses existing view routes without suggesting unavailable account or search behavior. | [Design system](../docs/design-system.md) |
| Shared footer | Category links point to `catalog.html`. Legal labels remain plain text until destination pages exist. Show a Contact section without fabricated contact data and use the approved academic copyright line. | Avoids fictitious destinations and contact information. | [Design system](../docs/design-system.md) |
| Home product placeholders | Reserve ten numbered spaces for best sellers, with image and price areas marked pending. Do not create new-arrival cards yet; show “Próximamente”. | Placeholder layout was approved, but actual product content has not been supplied. This leaves RF-004 and complete product cards unfinished. | [Home SPEC](../specs/01-home/spec.md), [Home tasks](../specs/01-home/task.md), [index.html](../index.html) |

## Pending decisions

- Hero campaign headline, descriptive copy, and approved image. The current visible copy is provisional; the campaign image is only a reserved area.
- Real product names, images, prices, and currency for the ten best-seller spaces.
- Whether and when to populate “Nuevos lanzamientos”; until approved, it remains “Próximamente”.
- Other views' detailed requirements and implementation decisions; consult their applicable specifications when available.

Record new decisions here only after explicit approval. Keep detailed acceptance criteria and implementation steps in their SPEC, PLAN, and task files; do not duplicate them here.
