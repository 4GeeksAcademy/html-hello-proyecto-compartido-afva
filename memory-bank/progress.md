# Progress — MAISON NOVA

Last reviewed: 2026-10-26

This status was checked against the current files. “Verified” means observed in the repository or checked with a stated validation; “documented decision” means approved and recorded but not necessarily implemented; “pending” means not verified or not yet supplied.

## Current state of the five views

| View | Verified current state | Remaining work |
| --- | --- | --- |
| Home (`index.html`) | Partially implemented. Semantic page shell, metadata, one `h1`, shared navigation/footer, hero layout, “Próximamente” new-arrivals section, and ten numbered best-seller placeholders are present. | Hero campaign content and real product data are missing; several Home tasks and manual validation remain open. Details below. |
| Catalog (`catalog.html`) | File exists and is empty. | Deferred to a later branch; not part of the current Home iteration. |
| Product (`product.html`) | File exists and is empty. | Deferred to a later branch; not part of the current Home iteration. |
| Cart (`cart.html`) | File exists and is empty. | Deferred to a later branch; not part of the current Home iteration. |
| Checkout (`checkout.html`) | File exists and is empty. | Deferred to a later branch; not part of the current Home iteration. |

## Home progress

### Verified implementation

- `index.html` contains HTML metadata, semantic `header` / `main` / `footer`, and one `h1`.
- Navigation uses local links to existing view files. The search is disabled and account access is visual-only.
- The hero layout and catalog CTA exist, but the campaign copy and image are not approved content.
- “Nuevos lanzamientos” has a “Próximamente” message and no product cards, as currently approved; RF-004 remains incomplete.
- “Más vendidos” has ten numbered placeholder cards. Image and price values are pending, so these are not complete product cards and RF-006 is not fully satisfied.
- Footer has the approved categories, non-linked legal labels, Contact section without invented details, and academic copyright text.
- Tailwind CSS v4 browser CDN and an Organization JSON-LD block are present.

### Task status

- **T-001, repository inspection:** checked in the task file; the five HTML files, asset directory, Tailwind convention, and active branch were inspected.
- **T-002, shared content/design decisions:** approved identity, navigation/footer, and placeholder policy are recorded; actual product data remains pending.
- **T-003, semantic structure and metadata:** checked; HTML parser and structural checks passed.
- **T-004, navbar:** markup and local destinations exist; manual keyboard/accessibility verification remains open.
- **T-005, hero:** pending. Layout exists, but approved campaign headline, copy, and image do not.
- **T-006, new arrivals:** section heading/state exists; no cards are approved or implemented, so the task is incomplete by design.
- **T-007, best sellers:** ten placeholder cards and responsive grid markup exist; approved names, images, and prices are absent, so the task is incomplete.
- **T-008, footer:** markup reflects approved footer content; visual/manual review is still part of overall validation.
- **T-009, responsive:** mobile-first and breakpoint classes are present; manual checks at 375, 768, and 1440 px have not been completed.
- **T-010, accessibility:** labels, landmarks, descriptive links, and focus styles are present in markup; keyboard, focus behavior, and contrast have not been manually tested.
- **T-011, SEO / Schema.org:** title, description, headings, and JSON-LD are present; JSON-LD parsing passed.
- **T-012, integration:** local target files exist, but the other four pages are empty; integrated navigation and browser rendering have not been verified.
- **T-013, review / PR:** not complete; no PR review or integration is recorded.

## Verifications performed

- `git diff --check` passed during the Home work.
- Python's standard `html.parser` parsed `index.html`.
- A structural check found ten `<article>` cards and exactly one `h1`.
- Local link targets were checked for file existence.
- The JSON-LD block parsed as JSON.
- No custom JavaScript or framework was added to the Home.
- `curl -I http://localhost:8000/index.html` returned HTTP 200, and the Tailwind CSS v4 CDN endpoint returned HTTP 200.
- The English, Spanish, and Chinese READMEs now describe the partial Home, approved placeholders, deferred views, `docs/design-system.md`, the Memory Bank, and the actual Home task filename `task.md`.

These are static/HTTP checks, not proof of visual behavior. A browser-open command was issued, but responsive rendering, loaded CDN styles in the rendered page, and actual usability were not manually confirmed. No Chromium, Firefox, Playwright, or Selenium installation is available in the environment for automated viewport checks.

## Pending work and blockers

- Approve a hero campaign headline, descriptive copy, and image; replace provisional text and the reserved image area, then complete T-005.
- Supply actual product names, images, prices, and currency for the ten best-seller cards.
- No new-arrival cards are approved for this iteration; keep “Próximamente” and leave T-006/RF-004 incomplete until products are approved or the SPEC is formally revised.
- Run visual checks at 375, 768, and 1440 px; test keyboard navigation, focus visibility, and contrast.
- Verify the rendered page and Tailwind CDN styles visually in a browser; check integrated routes when the other views are implemented.
- Complete the Home acceptance review and PR review when authorized.

## Recommended next steps

1. Keep placeholders until approved hero content and product data are supplied; do not invent copy, images, names, prices, or currency.
2. Implement only the newly approved content and update the applicable task evidence.
3. Run and record manual responsive, keyboard, contrast, and browser checks.
4. Reassess the Home acceptance criteria; do not treat placeholders as completed functionality. Start work on the other four views only on the later branch with approved SDD documents.
