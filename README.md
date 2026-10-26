# Fashion Store | E-commerce Prototype

## 1. Project description
Collaborative project developed as part of the AI Engineering course at 4Geeks Academy.

The goal is to build a visual prototype of an online store for a France-based clothing brand.

The prototype should provide a modern, consistent, and responsive experience while applying web development, SEO, accessibility, and Git collaboration best practices.

## 2. Objectives

- Develop five main e-commerce views.
- Create a consistent visual identity across all pages.
- Ensure responsive layouts for mobile, tablet, and desktop.
- Apply semantic HTML and SEO best practices.
- Add Schema.org structured data where appropriate.
- Practice collaborative development with Git, branches, and pull requests.
- Use Spec-Driven Development (SDD) to organize the work.

## 3. Functional scope

### 3.1 Home (`index.html`)

- Navbar with logo, search, and account menu.
- Campaign and featured-product hero section.
- New arrivals section.
- Best sellers section.
- Footer with categories, legal information, and contact details.

### 3.2 Catalog (`catalog.html`)

- Shared navbar and footer.
- Category and size filters.
- Reference grid of 4 columns and 5 rows, with 20 products.
- Links to product pages.

### 3.3 Product (`product.html`)

- Main product image.
- Name, reference, and price.
- Size and quantity selection.
- Add-to-cart button.
- Detailed description, materials, and recommended uses.

### 3.4 Cart (`cart.html`)

- Complete cart view.
- Three sample products.
- Thumbnails, prices, quantities, and totals for each product.
- Summary with subtotal, taxes, and total.
- Button to proceed to checkout.

### 3.5 Checkout (`checkout.html`)

Payment form visually divided into three steps:

1. Personal details.
2. Delivery address.
3. Card payment details.

Checkout is for demonstration only. It will not process real payments or store banking information.

## 4. Technologies

| Technology | Use |
| --- | --- |
| HTML5 | Structure and content |
| Tailwind CSS | Styling and responsive layouts |
| Schema.org | Structured data |
| Git | Version control |
| GitHub | Repository and collaboration |
| GitHub Codespaces | Development environment |

**Restriction:** Do not use React, Vue, Angular, custom JavaScript, a backend, or additional frameworks.

Interactions that require dynamic logic will be represented demonstratively with HTML, without suggesting functionality that has not been implemented.

## 5. Project structure

```
fashion-store/
├── AGENTS.md
├── CONTEXT.md
├── README.md
├── docs/
│   └── design-system.md
├── memory-bank/
│   ├── decisions.md
│   └── progress.md
├── index.html
├── catalog.html
├── product.html
├── cart.html
├── checkout.html
├── assets/
│   └── images/
└── specs/
    ├── 01-home/
    │   ├── spec.md
    │   ├── plan.md
    │   └── task.md
    ├── 02-catalog/
    ├── 03-product/
    ├── 04-cart/
    └── 05-checkout/
```

The Home currently has `spec.md`, `plan.md`, and `task.md` in `specs/01-home/`. The other view folders are deferred to a later branch and do not yet have approved SDD documents.

SDD documents define requirements, implementation strategy, and verifiable tasks for each approved view.

## 6. Development methodology

Spec-Driven Development (SDD) will be used:

1. **Context:** understand the project, scope, and constraints.
2. **SPEC:** define what must be built.
3. **PLAN:** determine how it will be implemented.
4. **TASKS:** break the work into verifiable tasks.
5. **Implementation:** develop the approved tasks.
6. **Validation:** check requirements, responsiveness, SEO, and accessibility.

AI agents must follow the instructions in `AGENTS.md`.

The Memory Bank in `memory-bank/` supports continuity between work sessions: `decisions.md` summarizes approved decisions and their sources, while `progress.md` records verified status, evidence, and pending work. These summaries do not replace the detailed specifications or plans.

## 7. Git collaboration

### Branch strategy

- `main`: stable project version.
- `develop`: integration branch for developers' work.
- `feature/*`: branches for individual features.

Examples:

```
feature/home
feature/catalog
feature/product
feature/cart
feature/checkout
```

### Workflow

1. Sync the `develop` branch.
2. Create a `feature/*` branch.
3. Develop the assigned feature.
4. Verify the changes.
5. Make descriptive commits.
6. Push the branch to GitHub.
7. Create a pull request targeting `develop`.
8. Request a review from the other developer.
9. Integrate the approved changes.

Do not make changes directly on `main` during regular development.

## 8. Development conventions

- Use semantic HTML5.
- Design mobile-first.
- Apply Tailwind CSS consistently.
- Use accessible elements and alternative text for images.
- Provide appropriate titles and meta descriptions on every page.
- Use descriptive names for files and assets.
- Keep the navbar, footer, and navigation consistent.
- Avoid unnecessary dependencies.
- Do not include real customer information or banking details.

## 9. Running the project

The project consists of static HTML files.

To view it:

1. Open the repository in GitHub Codespaces or a local editor.
2. Open `index.html` in a browser, or serve the folder using a static server available in the environment.
3. Navigate between the five views using their links.

No backend or build process is required.

## 10. General acceptance criteria

- All five views are implemented and linked.
- The navbar and footer have a consistent design.
- The site is responsive on mobile, tablet, and desktop.
- Semantic HTML is used.
- SEO and Schema.org best practices are applied.
- Sample products and prices are consistent across views.
- The prototype respects the technology restriction.
- Code is integrated and reviewed through Git and pull requests.

## 11. Project status

**Phase:** Home partially implemented on the `home` branch. Catalog, Product, Cart, and Checkout are deferred to a later branch and remain empty.

Approved for the current Home iteration:

- Provisional MAISON NOVA identity and shared navigation/footer, documented in `docs/design-system.md`.
- Ten numbered best-seller placeholders with image and price areas reserved.
- No new-arrival cards for now; that section displays “Coming soon”.

Pending:

- Approved hero campaign headline, copy, and image; current hero copy is provisional.
- Actual names, images, prices, and currency for the ten best-seller products.
- Manual responsive, browser-rendering, keyboard, and contrast checks.
- Specifications and implementation for the four deferred views.
- Responsibilities shared between the two developers.

## 12. Team

Collaborative project by two participants in the AI Engineering course at 4Geeks Academy.

Specific responsibilities will be defined before implementation begins.
